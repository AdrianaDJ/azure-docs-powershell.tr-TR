---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: da50845ff5012d466eed0c68103cdbd0baea4e7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917235"
---
# <span data-ttu-id="e95d3-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="e95d3-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="e95d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e95d3-102">SYNOPSIS</span></span>
<span data-ttu-id="e95d3-103">Azure 'da çalışan bir IaaS sanal makinesinde şifrelemeyi mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="e95d3-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="e95d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e95d3-104">SYNTAX</span></span>

### <span data-ttu-id="e95d3-105">SinglePassParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e95d3-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e95d3-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="e95d3-106">AADClientSecretParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e95d3-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="e95d3-107">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e95d3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e95d3-108">DESCRIPTION</span></span>
<span data-ttu-id="e95d3-109">**Set-AzVMDiskEncryptionExtension** cmdlet 'i, çalışan bir altyapıda Azure 'da hizmet (IaaS) sanal makinesi olarak şifrelemeyi olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="e95d3-109">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="e95d3-110">Bu cmdlet, sanal makineye disk şifrelemesi uzantısını yükleyerek şifrelemeyi mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="e95d3-110">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="e95d3-111">*Ad* parametresi belirtilmezse, Windows işletim sistemini veya Linux sanal makineleri için AzureDiskEncryptionForLinux çalıştıran sanal makinelerde varsayılan ad AzureDiskEncryption bir uzantı yüklenir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-111">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="e95d3-112">Bu cmdlet, şifrelemeyi etkinleştirme adımlarının sanal makinenin yeniden başlatılmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-112">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="e95d3-113">Bu cmdlet 'i çalıştırmadan önce çalışmanızı sanal makinede kaydetmeniz tavsiye edilir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-113">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="e95d3-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e95d3-114">EXAMPLES</span></span>

### <span data-ttu-id="e95d3-115">Örnek 1: şifrelemeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="e95d3-115">Example 1: Enable encryption</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="e95d3-116">Bu örnekte, AD kimlik bilgileri belirtilmeden şifrelemenin etkinleştirilmesi gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-116">This example demonstrates enabling encryption without specifying AD credentials.</span></span>   

### <span data-ttu-id="e95d3-117">Örnek 2: ardışık düzen girişiyle şifrelemeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="e95d3-117">Example 2: Enable encryption with pipelined input</span></span>
```
$params = New-Object PSObject -Property @{
    ResourceGroupName = "[resource-group-name]"
    VMName = "[vm-name]"
    DiskEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    DiskEncryptionKeyVaultUrl = "https://[keyvault-name].vault.azure.net"
    KeyEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    KeyEncryptionKeyUrl = "https://[keyvault-name].vault.azure.net/keys/[kekname]/[kek-unique-id]"
    VolumeType = "All"
}

$params | Set-AzVmDiskEncryptionExtension
```

<span data-ttu-id="e95d3-118">Bu örnekte, AD kimlik bilgilerini belirtmeden şifrelemeyi etkinleştirmek için ardışık işlem kullanan giriş kullanılarak parametrelerin gönderilmesi gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-118">This example demonstrates sending parameters using pipelined input to enable encryption without specifying AD credentials.</span></span>  

### <span data-ttu-id="e95d3-119">Örnek 3: Azure AD Istemci KIMLIĞINI ve Istemci gizliliğini kullanarak şifrelemeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="e95d3-119">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
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

<span data-ttu-id="e95d3-120">Bu örnekte, Azure AD istemci KIMLIĞI ve istemci parolası kullanılarak şifreleme etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-120">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="e95d3-121">Örnek 4: Azure AD İstemci KIMLIĞINI ve istemci sertifikası parmak izini kullanarak şifrelemeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="e95d3-121">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
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
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue 
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
Set-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="e95d3-122">Bu örnek, Azure AD istemci KIMLIĞI ve istemci sertifikası parmak izleri kullanılarak şifrelemeyi sağlar.</span><span class="sxs-lookup"><span data-stu-id="e95d3-122">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="e95d3-123">Örnek 5: anahtar şifreleme anahtarını kullanarak Azure AD istemci KIMLIĞI, istemci parolası kullanarak şifrelemeyi etkinleştirme ve disk şifrelemesini sarma</span><span class="sxs-lookup"><span data-stu-id="e95d3-123">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="e95d3-124">Bu örnekte, anahtar şifreleme anahtarını kullanarak Azure AD İstemcisi KIMLIĞI, istemci parolası ve disk şifrelemesini kaydır kullanılarak şifreleme etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-124">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="e95d3-125">Örnek 6: anahtar şifreleme anahtarı kullanarak Azure AD istemci KIMLIĞI, istemci sertifikası parmak izi ve disk şifrelemesi</span><span class="sxs-lookup"><span data-stu-id="e95d3-125">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue
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
Set-AzKeyVaultSecret -VaultName $VaultName-Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl 
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="e95d3-126">Bu örnek, anahtar şifreleme anahtarı kullanılarak Azure AD istemci KIMLIĞI, istemci sertifikası parmak izi ve disk şifrelemesini kaydır ile şifrelemeyi olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="e95d3-126">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="e95d3-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e95d3-127">PARAMETERS</span></span>

### <span data-ttu-id="e95d3-128">-Aadclientcertparmak Izi</span><span class="sxs-lookup"><span data-stu-id="e95d3-128">-AadClientCertThumbprint</span></span>
<span data-ttu-id="e95d3-129">**Anahtar kasaya** gizli yazma Izinleri olan AzureActive Directory (Azure AD) uygulama istemcisi sertifikasının parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-129">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="e95d3-130">Önkoşul olarak, Azure AD İstemcisi sertifikasının daha önce sanal makinenin yerel bilgisayar `my` sertifika deposuna dağıtılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-130">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="e95d3-131">Azure 'daki bir sanal makineye sertifika dağıtmak için Add-AzVMSecret cmdlet 'i kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-131">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="e95d3-132">Daha fazla bilgi için **Add-AzVMSecret** cmdlet yardımına bakın.</span><span class="sxs-lookup"><span data-stu-id="e95d3-132">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="e95d3-133">Sertifika, daha önce sanal makine yerel bilgisayarına sertifika deponuza dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e95d3-133">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientCertParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-134">-Aadclitıd</span><span class="sxs-lookup"><span data-stu-id="e95d3-134">-AadClientID</span></span>
<span data-ttu-id="e95d3-135">**Anahtar kasaya** gizli yazma Izni olan Azure AD UYGULAMASıNıN istemci kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-135">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet, AADClientCertParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-136">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="e95d3-136">-AadClientSecret</span></span>
<span data-ttu-id="e95d3-137">**Anahtar kasaya** parola yazma Izinleri olan Azure AD uygulamasının istemci gizliliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-137">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e95d3-138">-DefaultProfile</span></span>
<span data-ttu-id="e95d3-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e95d3-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-140">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="e95d3-140">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="e95d3-141">Bu cmdlet 'in, uzantının ara sürümünün otomatik yükseltmesini devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-141">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-142">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="e95d3-142">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="e95d3-143">Sanal makine şifreleme anahtarlarının karşıya yüklenmesi gereken **tuş Kasası** kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-143">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-144">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="e95d3-144">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="e95d3-145">Sanal makine şifreleme anahtarlarının karşıya yüklenmesi gereken **tuş Kasası** URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-145">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-146">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="e95d3-146">-EncryptFormatAll</span></span>
<span data-ttu-id="e95d3-147">Şifrelenmemiş olan tüm veri sürücülerini Encrypt-Format</span><span class="sxs-lookup"><span data-stu-id="e95d3-147">Encrypt-Format all data drives that are not already encrypted</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-148">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="e95d3-148">-ExtensionPublisherName</span></span>
<span data-ttu-id="e95d3-149">Dahili yayımcı adı.</span><span class="sxs-lookup"><span data-stu-id="e95d3-149">The extension publisher name.</span></span> <span data-ttu-id="e95d3-150">Bu parametreyi yalnızca "Microsoft. Azure. Security" varsayılan değerini geçersiz kılmak için belirtin.</span><span class="sxs-lookup"><span data-stu-id="e95d3-150">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-151">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="e95d3-151">-ExtensionType</span></span>
<span data-ttu-id="e95d3-152">Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="e95d3-152">The extension type.</span></span> <span data-ttu-id="e95d3-153">Windows VM 'ler için "AzureDiskEncryption" varsayılan değerini (Linux VM 'Ler için "AzureDiskEncryptionForLinux" olarak geçersiz kılmak için bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="e95d3-153">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-154">-Force</span><span class="sxs-lookup"><span data-stu-id="e95d3-154">-Force</span></span>
<span data-ttu-id="e95d3-155">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e95d3-155">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-156">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e95d3-156">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="e95d3-157">Sanal makinenin anahtar şifrelemesini kaydırmak ve kaydırmak için kullanılan algoritmayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-157">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="e95d3-158">Varsayılan değer RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="e95d3-158">The default value is RSA-OAEP.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-159">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="e95d3-159">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="e95d3-160">Sanal makine şifreleme anahtarını kaydırmak ve kaydırmak için kullanılan anahtar şifreleme anahtarının URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-160">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="e95d3-161">Bu, tam sürümlü URL olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e95d3-161">This must be the full versioned URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-162">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="e95d3-162">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="e95d3-163">Sanal makine şifreleme anahtarını kaydırmak ve kaydırmak için kullanılan anahtar şifreleme anahtarını içeren tuş **Kasası** kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-163">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="e95d3-164">Bu, tam sürümlü bir URL olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e95d3-164">This must be a full versioned URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-165">-Ad</span><span class="sxs-lookup"><span data-stu-id="e95d3-165">-Name</span></span>
<span data-ttu-id="e95d3-166">Uzantıyı temsil eden Azure Resource Manager kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-166">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="e95d3-167">Varsayılan değer, Windows işletim sistemini veya Linux sanal makineleri için AzureDiskEncryptionForLinux çalıştıran sanal makinelerde AzureDiskEncryption.</span><span class="sxs-lookup"><span data-stu-id="e95d3-167">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-168">-Parola</span><span class="sxs-lookup"><span data-stu-id="e95d3-168">-Passphrase</span></span>
<span data-ttu-id="e95d3-169">Linux sanal makinelerini şifrelemek için kullanılan parolayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-169">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="e95d3-170">Bu parametre, Windows işletim sistemini çalıştıran sanal makinelerde kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="e95d3-170">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e95d3-171">-ResourceGroupName</span></span>
<span data-ttu-id="e95d3-172">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-172">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-173">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="e95d3-173">-SequenceVersion</span></span>
<span data-ttu-id="e95d3-174">Sanal makine için şifreleme işlemlerinin dizi sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-174">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="e95d3-175">Bu, aynı sanal makinede gerçekleştirilen her şifreleme işlemi için benzersizdir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-175">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="e95d3-176">Get-AzVMExtension cmdlet, kullanılan önceki seri numarasını almak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-176">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-177">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="e95d3-177">-SkipVmBackup</span></span>
<span data-ttu-id="e95d3-178">Linux VM 'Ler için yedekleme oluşturmayı atlama</span><span class="sxs-lookup"><span data-stu-id="e95d3-178">Skip backup creation for Linux VMs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-179">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="e95d3-179">-TypeHandlerVersion</span></span>
<span data-ttu-id="e95d3-180">Şifreleme uzantısının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-180">Specifies the version of the encryption extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-181">-VMName</span><span class="sxs-lookup"><span data-stu-id="e95d3-181">-VMName</span></span>
<span data-ttu-id="e95d3-182">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-182">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-183">-Birimtürü</span><span class="sxs-lookup"><span data-stu-id="e95d3-183">-VolumeType</span></span>
<span data-ttu-id="e95d3-184">Şifreleme işlemini gerçekleştirecek sanal makine birimlerinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-184">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="e95d3-185">Windows işletim sistemini çalıştıran sanal makinelere izin verilen değerler şunlardır: tümü, IŞLETIM sistemi ve veri.</span><span class="sxs-lookup"><span data-stu-id="e95d3-185">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="e95d3-186">Linux sanal makinelerinin izin verilen değerleri aşağıdaki gibidir: yalnızca veriler.</span><span class="sxs-lookup"><span data-stu-id="e95d3-186">The allowed values for Linux virtual machines are as follows: Data only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-187">-Onay</span><span class="sxs-lookup"><span data-stu-id="e95d3-187">-Confirm</span></span>
<span data-ttu-id="e95d3-188">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e95d3-188">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e95d3-189">-WhatIf</span></span>
<span data-ttu-id="e95d3-190">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e95d3-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e95d3-191">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e95d3-191">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e95d3-192">CommonParameters</span></span>
<span data-ttu-id="e95d3-193">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e95d3-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e95d3-194">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e95d3-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e95d3-195">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e95d3-195">INPUTS</span></span>

### <span data-ttu-id="e95d3-196">System. String</span><span class="sxs-lookup"><span data-stu-id="e95d3-196">System.String</span></span>

### <span data-ttu-id="e95d3-197">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e95d3-197">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e95d3-198">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e95d3-198">OUTPUTS</span></span>

### <span data-ttu-id="e95d3-199">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e95d3-199">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e95d3-200">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e95d3-200">NOTES</span></span>

## <span data-ttu-id="e95d3-201">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e95d3-201">RELATED LINKS</span></span>

[<span data-ttu-id="e95d3-202">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="e95d3-202">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="e95d3-203">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="e95d3-203">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="e95d3-204">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="e95d3-204">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


