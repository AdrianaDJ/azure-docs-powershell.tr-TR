---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMDiskEncryptionExtension.md
ms.openlocfilehash: 3eb2c1c175f52f980ecd451bb7a9474984543f18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590355"
---
# <span data-ttu-id="9cadf-101">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="9cadf-101">Set-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="9cadf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cadf-102">SYNOPSIS</span></span>
<span data-ttu-id="9cadf-103">Azure 'da çalışan bir IaaS sanal makinesinde şifrelemeyi mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="9cadf-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cadf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9cadf-104">SYNTAX</span></span>

### <span data-ttu-id="9cadf-105">SinglePassParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9cadf-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cadf-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cadf-106">AADClientSecretParameterSet</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cadf-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cadf-107">AADClientCertParameterSet</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cadf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9cadf-108">DESCRIPTION</span></span>
<span data-ttu-id="9cadf-109">**Set-AzureRmVMDiskEncryptionExtension** cmdlet 'i, çalışan bir altyapıda Azure 'da hizmet (IaaS) sanal makinesi olarak şifrelemeyi olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="9cadf-109">The **Set-AzureRmVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="9cadf-110">Bu cmdlet, sanal makineye disk şifrelemesi uzantısını yükleyerek şifrelemeyi mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="9cadf-110">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="9cadf-111">*Ad* parametresi belirtilmezse, Windows işletim sistemini veya Linux sanal makineleri için AzureDiskEncryptionForLinux çalıştıran sanal makinelerde varsayılan ad AzureDiskEncryption bir uzantı yüklenir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-111">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="9cadf-112">Bu cmdlet, şifrelemeyi etkinleştirme adımlarının sanal makinenin yeniden başlatılmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-112">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="9cadf-113">Bu cmdlet 'i çalıştırmadan önce çalışmanızı sanal makinede kaydetmeniz tavsiye edilir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-113">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="9cadf-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9cadf-114">EXAMPLES</span></span>

### <span data-ttu-id="9cadf-115">Örnek 1: şifrelemeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="9cadf-115">Example 1: Enable encryption</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="9cadf-116">Bu örnekte, AD kimlik bilgileri belirtilmeden şifrelemenin etkinleştirilmesi gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-116">This example demonstrates enabling encryption without specifying AD credentials.</span></span>

### <span data-ttu-id="9cadf-117">Örnek 2: ardışık düzen girişiyle şifrelemeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="9cadf-117">Example 2: Enable encryption with pipelined input</span></span>
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

$params | Set-AzureRmVmDiskEncryptionExtension
```

<span data-ttu-id="9cadf-118">Bu örnekte, AD kimlik bilgilerini belirtmeden şifrelemeyi etkinleştirmek için ardışık işlem kullanan giriş kullanılarak parametrelerin gönderilmesi gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-118">This example demonstrates sending parameters using pipelined input to enable encryption without specifying AD credentials.</span></span>

### <span data-ttu-id="9cadf-119">Örnek 3: Azure AD Istemci KIMLIĞINI ve Istemci gizliliğini kullanarak şifrelemeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="9cadf-119">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="9cadf-120">Bu örnekte, Azure AD istemci KIMLIĞI ve istemci parolası kullanılarak şifreleme etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-120">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="9cadf-121">Örnek 4: Azure AD İstemci KIMLIĞINI ve istemci sertifikası parmak izini kullanarak şifrelemeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="9cadf-121">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzureRmADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue
$ServicePrincipal = New-AzureRmADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

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
Set-AzureRmKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzureRmVM -ResourceGroupName $RGName -Name $VMName
$VM = Add-AzureRmVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzureRmVM -VM $VM -ResourceGroupName $RGName

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="9cadf-122">Bu örnek, Azure AD istemci KIMLIĞI ve istemci sertifikası parmak izleri kullanılarak şifrelemeyi sağlar.</span><span class="sxs-lookup"><span data-stu-id="9cadf-122">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="9cadf-123">Örnek 5: anahtar şifreleme anahtarını kullanarak Azure AD istemci KIMLIĞI, istemci parolası kullanarak şifrelemeyi etkinleştirme ve disk şifrelemesini sarma</span><span class="sxs-lookup"><span data-stu-id="9cadf-123">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="9cadf-124">Bu örnekte, anahtar şifreleme anahtarını kullanarak Azure AD İstemcisi KIMLIĞI, istemci parolası ve disk şifrelemesini kaydır kullanılarak şifreleme etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-124">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="9cadf-125">Örnek 6: anahtar şifreleme anahtarı kullanarak Azure AD istemci KIMLIĞI, istemci sertifikası parmak izi ve disk şifrelemesi</span><span class="sxs-lookup"><span data-stu-id="9cadf-125">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzureRmADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue
$ServicePrincipal = New-AzureRmADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

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
Set-AzureRmKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzureRmVM -ResourceGroupName $RGName -Name $VMName
$VM = Add-AzureRmVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzureRmVM -VM $VM -ResourceGroupName $RGName

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="9cadf-126">Bu örnek, anahtar şifreleme anahtarı kullanılarak Azure AD istemci KIMLIĞI, istemci sertifikası parmak izi ve disk şifrelemesini kaydır ile şifrelemeyi olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="9cadf-126">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="9cadf-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9cadf-127">PARAMETERS</span></span>

### <span data-ttu-id="9cadf-128">-Aadclientcertparmak Izi</span><span class="sxs-lookup"><span data-stu-id="9cadf-128">-AadClientCertThumbprint</span></span>
<span data-ttu-id="9cadf-129">**Anahtar kasaya** gizli yazma Izinleri olan AzureActive Directory (Azure AD) uygulama istemcisi sertifikasının parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-129">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="9cadf-130">Önkoşul olarak, Azure AD İstemcisi sertifikasının daha önce sanal makinenin yerel bilgisayar `my` sertifika deposuna dağıtılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-130">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="9cadf-131">Azure 'daki bir sanal makineye sertifika dağıtmak için Add-AzureRmVMSecret cmdlet 'i kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-131">The Add-AzureRmVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="9cadf-132">Daha fazla bilgi için **Add-AzureRmVMSecret** cmdlet yardımına bakın.</span><span class="sxs-lookup"><span data-stu-id="9cadf-132">For more details, see the **Add-AzureRmVMSecret** cmdlet help.</span></span>
<span data-ttu-id="9cadf-133">Sertifika, daha önce sanal makine yerel bilgisayarına sertifika deponuza dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9cadf-133">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

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

### <span data-ttu-id="9cadf-134">-Aadclitıd</span><span class="sxs-lookup"><span data-stu-id="9cadf-134">-AadClientID</span></span>
<span data-ttu-id="9cadf-135">**Anahtar kasaya** gizli yazma Izni olan Azure AD UYGULAMASıNıN istemci kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-135">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="9cadf-136">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="9cadf-136">-AadClientSecret</span></span>
<span data-ttu-id="9cadf-137">**Anahtar kasaya** parola yazma Izinleri olan Azure AD uygulamasının istemci gizliliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-137">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="9cadf-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cadf-138">-DefaultProfile</span></span>
<span data-ttu-id="9cadf-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9cadf-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cadf-140">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="9cadf-140">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="9cadf-141">Bu cmdlet 'in, uzantının ara sürümünün otomatik yükseltmesini devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-141">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="9cadf-142">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="9cadf-142">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="9cadf-143">Sanal makine şifreleme anahtarlarının karşıya yüklenmesi gereken **tuş Kasası** kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-143">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="9cadf-144">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="9cadf-144">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="9cadf-145">Sanal makine şifreleme anahtarlarının karşıya yüklenmesi gereken **tuş Kasası** URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-145">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="9cadf-146">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="9cadf-146">-EncryptFormatAll</span></span>
<span data-ttu-id="9cadf-147">Şifrelenmemiş olan tüm veri sürücülerini Encrypt-Format</span><span class="sxs-lookup"><span data-stu-id="9cadf-147">Encrypt-Format all data drives that are not already encrypted</span></span>

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

### <span data-ttu-id="9cadf-148">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="9cadf-148">-ExtensionPublisherName</span></span>
<span data-ttu-id="9cadf-149">Dahili yayımcı adı.</span><span class="sxs-lookup"><span data-stu-id="9cadf-149">The extension publisher name.</span></span> <span data-ttu-id="9cadf-150">Bu parametreyi yalnızca "Microsoft. Azure. Security" varsayılan değerini geçersiz kılmak için belirtin.</span><span class="sxs-lookup"><span data-stu-id="9cadf-150">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="9cadf-151">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="9cadf-151">-ExtensionType</span></span>
<span data-ttu-id="9cadf-152">Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="9cadf-152">The extension type.</span></span> <span data-ttu-id="9cadf-153">Windows VM 'ler için "AzureDiskEncryption" varsayılan değerini (Linux VM 'Ler için "AzureDiskEncryptionForLinux" olarak geçersiz kılmak için bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="9cadf-153">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="9cadf-154">-Force</span><span class="sxs-lookup"><span data-stu-id="9cadf-154">-Force</span></span>
<span data-ttu-id="9cadf-155">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="9cadf-155">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9cadf-156">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="9cadf-156">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="9cadf-157">Sanal makinenin anahtar şifrelemesini kaydırmak ve kaydırmak için kullanılan algoritmayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-157">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="9cadf-158">Varsayılan değer RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="9cadf-158">The default value is RSA-OAEP.</span></span>

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

### <span data-ttu-id="9cadf-159">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="9cadf-159">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="9cadf-160">Sanal makine şifreleme anahtarını kaydırmak ve kaydırmak için kullanılan anahtar şifreleme anahtarının URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-160">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="9cadf-161">Bu, tam sürümlü URL olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9cadf-161">This must be the full versioned URL.</span></span>

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

### <span data-ttu-id="9cadf-162">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="9cadf-162">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="9cadf-163">Sanal makine şifreleme anahtarını kaydırmak ve kaydırmak için kullanılan anahtar şifreleme anahtarını içeren tuş **Kasası** kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-163">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="9cadf-164">Bu, tam sürümlü bir URL olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9cadf-164">This must be a full versioned URL.</span></span>

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

### <span data-ttu-id="9cadf-165">-Ad</span><span class="sxs-lookup"><span data-stu-id="9cadf-165">-Name</span></span>
<span data-ttu-id="9cadf-166">Uzantıyı temsil eden Azure Resource Manager kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-166">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="9cadf-167">Varsayılan değer, Windows işletim sistemini veya Linux sanal makineleri için AzureDiskEncryptionForLinux çalıştıran sanal makinelerde AzureDiskEncryption.</span><span class="sxs-lookup"><span data-stu-id="9cadf-167">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

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

### <span data-ttu-id="9cadf-168">-Parola</span><span class="sxs-lookup"><span data-stu-id="9cadf-168">-Passphrase</span></span>
<span data-ttu-id="9cadf-169">Linux sanal makinelerini şifrelemek için kullanılan parolayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-169">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="9cadf-170">Bu parametre, Windows işletim sistemini çalıştıran sanal makinelerde kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="9cadf-170">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="9cadf-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cadf-171">-ResourceGroupName</span></span>
<span data-ttu-id="9cadf-172">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-172">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9cadf-173">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="9cadf-173">-SequenceVersion</span></span>
<span data-ttu-id="9cadf-174">Sanal makine için şifreleme işlemlerinin dizi sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-174">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="9cadf-175">Bu, aynı sanal makinede gerçekleştirilen her şifreleme işlemi için benzersizdir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-175">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="9cadf-176">Get-AzureRmVMExtension cmdlet, kullanılan önceki seri numarasını almak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-176">The Get-AzureRmVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

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

### <span data-ttu-id="9cadf-177">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="9cadf-177">-SkipVmBackup</span></span>
<span data-ttu-id="9cadf-178">Linux VM 'Ler için yedekleme oluşturmayı atlama</span><span class="sxs-lookup"><span data-stu-id="9cadf-178">Skip backup creation for Linux VMs</span></span>

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

### <span data-ttu-id="9cadf-179">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="9cadf-179">-TypeHandlerVersion</span></span>
<span data-ttu-id="9cadf-180">Şifreleme uzantısının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-180">Specifies the version of the encryption extension.</span></span>

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

### <span data-ttu-id="9cadf-181">-VMName</span><span class="sxs-lookup"><span data-stu-id="9cadf-181">-VMName</span></span>
<span data-ttu-id="9cadf-182">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-182">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="9cadf-183">-Birimtürü</span><span class="sxs-lookup"><span data-stu-id="9cadf-183">-VolumeType</span></span>
<span data-ttu-id="9cadf-184">Şifreleme işlemini gerçekleştirecek sanal makine birimlerinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-184">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="9cadf-185">Windows işletim sistemini çalıştıran sanal makinelere izin verilen değerler şunlardır: tümü, IŞLETIM sistemi ve veri.</span><span class="sxs-lookup"><span data-stu-id="9cadf-185">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="9cadf-186">Linux sanal makinelerinin izin verilen değerleri aşağıdaki gibidir: tüm, işletim sistemleri ve veriler Linux dağılımı tarafından desteklendiğindedir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-186">The allowed values for Linux virtual machines are as follows: All, OS, and Data when supported by the Linux distribution.</span></span>

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

### <span data-ttu-id="9cadf-187">-Onay</span><span class="sxs-lookup"><span data-stu-id="9cadf-187">-Confirm</span></span>
<span data-ttu-id="9cadf-188">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9cadf-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cadf-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cadf-189">-WhatIf</span></span>
<span data-ttu-id="9cadf-190">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9cadf-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cadf-191">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9cadf-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cadf-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cadf-192">CommonParameters</span></span>
<span data-ttu-id="9cadf-193">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9cadf-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cadf-194">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cadf-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cadf-195">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9cadf-195">INPUTS</span></span>

### <span data-ttu-id="9cadf-196">System. String</span><span class="sxs-lookup"><span data-stu-id="9cadf-196">System.String</span></span>

### <span data-ttu-id="9cadf-197">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9cadf-197">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9cadf-198">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9cadf-198">OUTPUTS</span></span>

### <span data-ttu-id="9cadf-199">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9cadf-199">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9cadf-200">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9cadf-200">NOTES</span></span>

## <span data-ttu-id="9cadf-201">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9cadf-201">RELATED LINKS</span></span>

[<span data-ttu-id="9cadf-202">Add-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="9cadf-202">Add-AzureRmVMSecret</span></span>](./Add-AzureRmVMSecret.md)

[<span data-ttu-id="9cadf-203">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="9cadf-203">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="9cadf-204">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="9cadf-204">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)


