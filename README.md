Repozytorium przykładowe mające na celu pokazać możliwości automatyzacji codziennych czynności - w tym przypadku konfiguracja maszyn z rozdziny Windows

Każdy obsługiwany Windowsowy host winien mieć skonfigurowaną usługę WinRM do komunikowania się z serwerem Ansible, zgodnie z dokumentacją wystarczy uruchomienie skryptu:
https://github.com/ansible/ansible/blob/devel/examples/scripts/ConfigureRemotingForAnsible.ps1

Hasło do użytkownika z uprawnieniami administratorskimi - winuser - jest zaszyfrowane, przy wywoływaniu polecenia należy dodać opcję --vault-id vault_secret 
np. ansible -m win_ping -i hosts laptopy --vault-id vault_secret




