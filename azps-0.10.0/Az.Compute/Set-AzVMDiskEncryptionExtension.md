---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: d4eb596ed7c6a002239b6e30869830596beba230
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936831"
---
# <span data-ttu-id="574a2-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="574a2-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="574a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="574a2-102">SYNOPSIS</span></span>
<span data-ttu-id="574a2-103">Azure 'da çalışan bir IaaS sanal makinesinde şifrelemeyi mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="574a2-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="574a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="574a2-104">SYNTAX</span></span>

### <span data-ttu-id="574a2-105">AADClientSecretParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="574a2-105">AADClientSecretParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="574a2-106">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="574a2-106">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="574a2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="574a2-107">DESCRIPTION</span></span>
<span data-ttu-id="574a2-108">**Set-AzVMDiskEncryptionExtension** cmdlet 'i, çalışan bir altyapıda Azure 'da hizmet (IaaS) sanal makinesi olarak şifrelemeyi olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="574a2-108">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="574a2-109">Bu cmdlet, sanal makineye disk şifrelemesi uzantısını yükleyerek şifrelemeyi mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="574a2-109">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="574a2-110">*Ad* parametresi belirtilmezse, Windows işletim sistemini veya Linux sanal makineleri için AzureDiskEncryptionForLinux çalıştıran sanal makinelerde varsayılan ad AzureDiskEncryption bir uzantı yüklenir.</span><span class="sxs-lookup"><span data-stu-id="574a2-110">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="574a2-111">Bu cmdlet, şifrelemeyi etkinleştirme adımlarının sanal makinenin yeniden başlatılmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="574a2-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="574a2-112">Bu cmdlet 'i çalıştırmadan önce çalışmanızı sanal makinede kaydetmeniz tavsiye edilir.</span><span class="sxs-lookup"><span data-stu-id="574a2-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="574a2-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="574a2-113">EXAMPLES</span></span>

### <span data-ttu-id="574a2-114">Örnek 1: Azure AD Istemci KIMLIĞINI ve Istemci gizliliğini kullanarak şifrelemeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="574a2-114">Example 1: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="574a2-115">Bu örnekte, Azure AD istemci KIMLIĞI ve istemci parolası kullanılarak şifreleme etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="574a2-115">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="574a2-116">Örnek 2: Azure AD İstemci KIMLIĞINI ve istemci sertifikası parmak izini kullanarak şifrelemeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="574a2-116">Example 2: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$KeyValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -KeyValue $KeyValue -KeyType AsymmetricX509Cert 
$ServicePrincipal = New-AzADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$aadClientCertThumbprint= $cert.Thumbprint

#Upload pfx to KeyVault 
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($fileContentBytes)
$JSONObject = @"
    { 
        "data" : "$filecontentencoded", 
        "dataType" : "pfx", 
        "password" : "$CertPassword" 
    } 
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($jsonObject)
$JSONEncoded = [System.Convert]::ToBase64String($jsonObjectBytes)

$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="574a2-117">Bu örnek, Azure AD istemci KIMLIĞI ve istemci sertifikası parmak izleri kullanılarak şifrelemeyi sağlar.</span><span class="sxs-lookup"><span data-stu-id="574a2-117">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="574a2-118">Örnek 3: anahtar şifreleme anahtarını kullanarak Azure AD istemci KIMLIĞI, istemci parolası kullanarak şifrelemeyi etkinleştirme ve disk şifrelemesini sarma</span><span class="sxs-lookup"><span data-stu-id="574a2-118">Example 3: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="574a2-119">Bu örnekte, anahtar şifreleme anahtarını kullanarak Azure AD İstemcisi KIMLIĞI, istemci parolası ve disk şifrelemesini kaydır kullanılarak şifreleme etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="574a2-119">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="574a2-120">Örnek 4: anahtar şifreleme anahtarı kullanarak Azure AD istemci KIMLIĞI, istemci sertifikası parmak izi ve disk şifrelemesi</span><span class="sxs-lookup"><span data-stu-id="574a2-120">Example 4: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$KeyValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -KeyValue $KeyValue -KeyType AsymmetricX509Cert 
$ServicePrincipal = New-AzADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$AADClientCertThumbprint= $Cert.Thumbprint

#Upload pfx to KeyVault 
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($FileContentBytes)
$JSONObject = @"
    { 
        "data" : "$filecontentencoded", 
        "dataType" : "pfx", 
        "password" : "$CertPassword" 
    } 
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($JSONObject)
$JsonEncoded = [System.Convert]::ToBase64String($JSONObjectBytes)
$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzureKeyVaultSecret -VaultName $VaultName-Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl 
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="574a2-121">Bu örnek, anahtar şifreleme anahtarı kullanılarak Azure AD istemci KIMLIĞI, istemci sertifikası parmak izi ve disk şifrelemesini kaydır ile şifrelemeyi olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="574a2-121">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="574a2-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="574a2-122">PARAMETERS</span></span>

### <span data-ttu-id="574a2-123">-Aadclientcertparmak Izi</span><span class="sxs-lookup"><span data-stu-id="574a2-123">-AadClientCertThumbprint</span></span>
<span data-ttu-id="574a2-124">**Anahtar kasaya** gizli yazma Izinleri olan AzureActive Directory (Azure AD) uygulama istemcisi sertifikasının parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="574a2-124">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="574a2-125">Önkoşul olarak, Azure AD İstemcisi sertifikasının daha önce sanal makinenin yerel bilgisayar `my` sertifika deposuna dağıtılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="574a2-125">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="574a2-126">Azure 'daki bir sanal makineye sertifika dağıtmak için Add-AzVMSecret cmdlet 'i kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="574a2-126">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="574a2-127">Daha fazla bilgi için **Add-AzVMSecret** cmdlet yardımına bakın.</span><span class="sxs-lookup"><span data-stu-id="574a2-127">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="574a2-128">Sertifika, daha önce sanal makine yerel bilgisayarına sertifika deponuza dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="574a2-128">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: String
Parameter Sets: AADClientCertParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-129">-Aadclitıd</span><span class="sxs-lookup"><span data-stu-id="574a2-129">-AadClientID</span></span>
<span data-ttu-id="574a2-130">**Anahtar kasaya** gizli yazma Izni olan Azure AD UYGULAMASıNıN istemci kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="574a2-130">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-131">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="574a2-131">-AadClientSecret</span></span>
<span data-ttu-id="574a2-132">**Anahtar kasaya** parola yazma Izinleri olan Azure AD uygulamasının istemci gizliliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="574a2-132">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: String
Parameter Sets: AADClientSecretParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="574a2-133">-DefaultProfile</span></span>
<span data-ttu-id="574a2-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="574a2-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-135">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="574a2-135">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="574a2-136">Bu cmdlet 'in, uzantının ara sürümünün otomatik yükseltmesini devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="574a2-136">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-137">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="574a2-137">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="574a2-138">Sanal makine şifreleme anahtarlarının karşıya yüklenmesi gereken **tuş Kasası** kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="574a2-138">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-139">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="574a2-139">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="574a2-140">Sanal makine şifreleme anahtarlarının karşıya yüklenmesi gereken **tuş Kasası** URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="574a2-140">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-141">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="574a2-141">-EncryptFormatAll</span></span>
<span data-ttu-id="574a2-142">Şifrelenmemiş olan tüm veri sürücülerini Encrypt-Format</span><span class="sxs-lookup"><span data-stu-id="574a2-142">Encrypt-Format all data drives that are not already encrypted</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-143">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="574a2-143">-ExtensionPublisherName</span></span>
<span data-ttu-id="574a2-144">Dahili yayımcı adı.</span><span class="sxs-lookup"><span data-stu-id="574a2-144">The extension publisher name.</span></span> <span data-ttu-id="574a2-145">Bu parametreyi yalnızca "Microsoft. Azure. Security" varsayılan değerini geçersiz kılmak için belirtin.</span><span class="sxs-lookup"><span data-stu-id="574a2-145">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-146">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="574a2-146">-ExtensionType</span></span>
<span data-ttu-id="574a2-147">Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="574a2-147">The extension type.</span></span> <span data-ttu-id="574a2-148">Windows VM 'ler için "AzureDiskEncryption" varsayılan değerini (Linux VM 'Ler için "AzureDiskEncryptionForLinux" olarak geçersiz kılmak için bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="574a2-148">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-149">-Force</span><span class="sxs-lookup"><span data-stu-id="574a2-149">-Force</span></span>
<span data-ttu-id="574a2-150">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="574a2-150">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-151">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="574a2-151">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="574a2-152">Sanal makinenin anahtar şifrelemesini kaydırmak ve kaydırmak için kullanılan algoritmayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="574a2-152">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="574a2-153">Varsayılan değer RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="574a2-153">The default value is RSA-OAEP.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-154">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="574a2-154">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="574a2-155">Sanal makine şifreleme anahtarını kaydırmak ve kaydırmak için kullanılan anahtar şifreleme anahtarının URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="574a2-155">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="574a2-156">Bu, tam sürümlü URL olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="574a2-156">This must be the full versioned URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-157">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="574a2-157">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="574a2-158">Sanal makine şifreleme anahtarını kaydırmak ve kaydırmak için kullanılan anahtar şifreleme anahtarını içeren tuş **Kasası** kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="574a2-158">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="574a2-159">Bu, tam sürümlü bir URL olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="574a2-159">This must be a full versioned URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-160">-Ad</span><span class="sxs-lookup"><span data-stu-id="574a2-160">-Name</span></span>
<span data-ttu-id="574a2-161">Uzantıyı temsil eden Azure Resource Manager kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="574a2-161">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="574a2-162">Varsayılan değer, Windows işletim sistemini veya Linux sanal makineleri için AzureDiskEncryptionForLinux çalıştıran sanal makinelerde AzureDiskEncryption.</span><span class="sxs-lookup"><span data-stu-id="574a2-162">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-163">-Parola</span><span class="sxs-lookup"><span data-stu-id="574a2-163">-Passphrase</span></span>
<span data-ttu-id="574a2-164">Linux sanal makinelerini şifrelemek için kullanılan parolayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="574a2-164">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="574a2-165">Bu parametre, Windows işletim sistemini çalıştıran sanal makinelerde kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="574a2-165">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="574a2-166">-ResourceGroupName</span></span>
<span data-ttu-id="574a2-167">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="574a2-167">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-168">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="574a2-168">-SequenceVersion</span></span>
<span data-ttu-id="574a2-169">Sanal makine için şifreleme işlemlerinin dizi sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="574a2-169">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="574a2-170">Bu, aynı sanal makinede gerçekleştirilen her şifreleme işlemi için benzersizdir.</span><span class="sxs-lookup"><span data-stu-id="574a2-170">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="574a2-171">Get-AzVMExtension cmdlet, kullanılan önceki seri numarasını almak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="574a2-171">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-172">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="574a2-172">-SkipVmBackup</span></span>
<span data-ttu-id="574a2-173">Linux VM 'Ler için yedekleme oluşturmayı atlama</span><span class="sxs-lookup"><span data-stu-id="574a2-173">Skip backup creation for Linux VMs</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-174">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="574a2-174">-TypeHandlerVersion</span></span>
<span data-ttu-id="574a2-175">Şifreleme uzantısının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="574a2-175">Specifies the version of the encryption extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-176">-VMName</span><span class="sxs-lookup"><span data-stu-id="574a2-176">-VMName</span></span>
<span data-ttu-id="574a2-177">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="574a2-177">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-178">-Birimtürü</span><span class="sxs-lookup"><span data-stu-id="574a2-178">-VolumeType</span></span>
<span data-ttu-id="574a2-179">Şifreleme işlemini gerçekleştirecek sanal makine birimlerinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="574a2-179">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="574a2-180">Windows işletim sistemini çalıştıran sanal makinelere izin verilen değerler şunlardır: tümü, IŞLETIM sistemi ve veri.</span><span class="sxs-lookup"><span data-stu-id="574a2-180">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="574a2-181">Linux sanal makinelerinin izin verilen değerleri aşağıdaki gibidir: yalnızca veriler.</span><span class="sxs-lookup"><span data-stu-id="574a2-181">The allowed values for Linux virtual machines are as follows: Data only.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-182">-Onay</span><span class="sxs-lookup"><span data-stu-id="574a2-182">-Confirm</span></span>
<span data-ttu-id="574a2-183">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="574a2-183">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="574a2-184">-WhatIf</span></span>
<span data-ttu-id="574a2-185">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="574a2-185">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="574a2-186">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="574a2-186">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="574a2-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="574a2-187">CommonParameters</span></span>
<span data-ttu-id="574a2-188">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="574a2-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="574a2-189">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="574a2-189">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="574a2-190">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="574a2-190">INPUTS</span></span>

### <span data-ttu-id="574a2-191">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="574a2-191">None</span></span>
<span data-ttu-id="574a2-192">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="574a2-192">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="574a2-193">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="574a2-193">OUTPUTS</span></span>

### <span data-ttu-id="574a2-194">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="574a2-194">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="574a2-195">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="574a2-195">NOTES</span></span>

## <span data-ttu-id="574a2-196">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="574a2-196">RELATED LINKS</span></span>

[<span data-ttu-id="574a2-197">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="574a2-197">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="574a2-198">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="574a2-198">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="574a2-199">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="574a2-199">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


