Repozytorium przykładowe mające na celu pokazać możliwości automatyzacji codziennych czynności - w tym przypadku konfiguracja maszyn z rozdziny Windows

Każdy obsługiwany Windowsowy host winien mieć skonfigurowaną usługę WinRM do komunikowania się z serwerem Ansible, zgodnie z dokumentacją wystarczy uruchomienie skryptu:
https://github.com/ansible/ansible/blob/devel/examples/scripts/ConfigureRemotingForAnsible.ps1

Hasła do użytkowników/programów są zaszyfrowane w pliku group_vars/all/passwords, przy wywoływaniu scenariusza należy dodać opcję --ask-vault-pass (zostaniemy poproszeni o podanie ustawionego hasła do deszyfrowania)
np. ansible -m win_ping -i hosts laptopy --ask-vault-pass
ansible-playbook FullConfiguration.yml --ask-vault-pass




