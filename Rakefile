#!/usr/bin/env rake
# frozen_string_literal: true

require './lib/vasevius_bot'

namespace :vasevius_bot do
  desc 'task to keep heroku service awake'
  task :keep_heroku_awake do
    begin
      response = RestClient.get("#{ENV['HEROKU_SERVICE_URL']}")
    rescue RestClient::Exception => e
      error = e
    end
  end
end
