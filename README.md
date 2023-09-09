# LogEase: Simplified Logging with Monolog

## Introduction

LogEase is a PHP library that simplifies the process of logging using the Monolog library. This library aims to provide an easy-to-use interface for storing, viewing, downloading log files, and displaying logs in your PHP applications.


## Features

- Easy setup and configuration.
- Log messages with various severity levels.
- View and download log files directly from your application.
- Display logs in your application's interface.

## Installation

To Use LogEase, First install monolog using composer:

```bash
composer require monolog/monolog
```
Add this line your PHP file - This will automatically create a logs and use logfile name as your php file name

```php
require_once 'LogEase.php'; 
$LogEase = new LogEase(); 
$LogEase->info("This is info log!" );
$LogEase->error("This is error log!" );
$LogEase->debug("This is debug log!" ,['test'=>'test']);
$LogEase->display_logs(); // To enable showing logs

$delete_before_days = 7;
$LogEase->auto_delete_log(7); // to delete log files by given days

echo PHP_EOL . $LogEase->get_log_url(); // print log file url
```
