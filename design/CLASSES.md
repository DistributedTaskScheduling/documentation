This file lists classes that will need to be included in our design.
Classes and packages are represented by headers followed by a short description.
Nested headers imply that a class will only ever be used inside another class.


# Package: CentralServer
Package for classes used exclusively on the central server.

## Class: JobCenter
Main class for the central server.
### Class: CentralServerCLIHandler
Sub-class of CLIHandler.
Processes CLI commands for the central server.
### Class: CentralServerConfig
Sub-class of Config.
Handles hierarchical configuration files for the central server.
### Class: Database
Wrapper around some database Python package that gives a clean interface.
### Class: Dispatcher
Provides a mechanism for distributing jobs to work machines.
### Class: Notifier
Sends notification to users.
### Class: Scheduler
Provides a strategy for distributing jobs to work machines.
### Class: WebAPI
Provides an interface to the TV group.
Provides information about server statistics.

## Class: LocalJobAdder
Python file that handles messages from user clients.


# Package: Common
Package for classes used by at least two out of: central server, user client, worker client.

## Class: CLIHandler
Sub-class of CLIHandler.
Abstract base class for handling CLI commands.

## Class: Config
Abstract base class for hierarchical configuration files.

## Class: JobMessage
Sub-class of Message for user jobs.

## Class: Message
Abstract base class for objects transferable via SSHConnection

## Class: SSHConnection
Class for handling connections between central server, user client, worker client.


# Package: UserClient
Package for classes used exclusively on the user client.

## Class: JobAdder
Main class for the user client.
### Class: UserClientCLIHandler
Sub-class of CLIHandler.
Processes CLI commands for the user client.
### Class: UserClientConfig
Sub-class of Config.
Handles hierarchical configuration files for the user client.


# Package: WorkerClient
Package for classes used exclusively on the worker client.

## Class: JobWorker
Main class for the worker client.
### Class: DockerWrapper
Wrapper class for Docker that gives us a clean interface.
### Class: Job
Realization of a user job.
### Class: WorkerClientCLIHandler
Sub-class of CLIHandler.
Processes CLI commands for the worker client.
### Class: WorkerClientConfig
Sub-class of Config.
Handles hierarchical configuration files for the worker client.
