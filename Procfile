api: cd evercam-api && bundle exec unicorn -p 9292 -c ./config/unicorn.rb
sidekiq: cd evercam-api && bundle exec sidekiq -c 5  -r ./scripts/sidekiq_setup.rb -C ./config/sidekiq.yml
dash: cd evercam-dashboard && EVERCAM_LOCAL=true bundle exec rails s
media: cd evercam-media && mix phoenix.server
