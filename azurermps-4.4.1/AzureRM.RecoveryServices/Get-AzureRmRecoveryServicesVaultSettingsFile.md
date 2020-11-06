---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 603cd65195f9e33c5006dcb4f2dc98ffc64aa7a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593027"
---
# <span data-ttu-id="66f81-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="66f81-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="66f81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66f81-102">SYNOPSIS</span></span>
<span data-ttu-id="66f81-103">Azure Site Recovery kasa ayarları dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="66f81-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66f81-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66f81-104">SYNTAX</span></span>

### <span data-ttu-id="66f81-105">Forsıte</span><span class="sxs-lookup"><span data-stu-id="66f81-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="66f81-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="66f81-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66f81-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="66f81-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66f81-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="66f81-108">DESCRIPTION</span></span>
<span data-ttu-id="66f81-109">**Get-Azurermrecoveryservicesvaultsettingsfıle** cmdlet 'i, bir Azure Site Recovery Kasası için ayarlar dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="66f81-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="66f81-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66f81-110">EXAMPLES</span></span>

### <span data-ttu-id="66f81-111">Örnek 1: Azure yedekleme için Windows Server veya DPM makinesini kaydettirme</span><span class="sxs-lookup"><span data-stu-id="66f81-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="66f81-112">İlk komut Testkasası adlı kasayı alır ve $Vault 01 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="66f81-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="66f81-113">İkinci komut $CredsPath değişkenini C:\downloadolarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="66f81-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>

<span data-ttu-id="66f81-114">Son komut, Azure yedekleme için $CredsPath 'daki kimlik bilgilerini kullanarak $Vault 01 kasa kimlik bilgileri dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="66f81-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

## <span data-ttu-id="66f81-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66f81-115">PARAMETERS</span></span>

### <span data-ttu-id="66f81-116">-Yedekleme</span><span class="sxs-lookup"><span data-stu-id="66f81-116">-Backup</span></span>
<span data-ttu-id="66f81-117">Kasa kimlik bilgileri dosyasının Azure yedekleme 'ye uygun olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="66f81-117">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f81-118">-Yol</span><span class="sxs-lookup"><span data-stu-id="66f81-118">-Path</span></span>
<span data-ttu-id="66f81-119">Azure Site Recovery kasa ayarları dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="66f81-119">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="66f81-120">Bu dosyayı Azure Site Recovery kasa portalından indirebilir ve yerel olarak depolayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="66f81-120">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f81-121">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="66f81-121">-SiteFriendlyName</span></span>
<span data-ttu-id="66f81-122">Sitenin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="66f81-122">Specifies the site friendly name.</span></span>
<span data-ttu-id="66f81-123">Bir Hyper-V sitesinin kasa kimlik bilgilerini indiriyorsunuz bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="66f81-123">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f81-124">-Sitetanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="66f81-124">-SiteIdentifier</span></span>
<span data-ttu-id="66f81-125">Site tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="66f81-125">Specifies the site identifier.</span></span>
<span data-ttu-id="66f81-126">Bir Hyper-V sitesinin kasa kimlik bilgilerini indiriyorsunuz bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="66f81-126">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f81-127">-Siterecoçok</span><span class="sxs-lookup"><span data-stu-id="66f81-127">-SiteRecovery</span></span>
<span data-ttu-id="66f81-128">Kasa kimlik bilgileri dosyasının Azure Site Recovery için geçerli olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="66f81-128">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f81-129">-Kasa</span><span class="sxs-lookup"><span data-stu-id="66f81-129">-Vault</span></span>
<span data-ttu-id="66f81-130">Azure Site Recovery kasa nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="66f81-130">Specifies the Azure Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66f81-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66f81-131">-DefaultProfile</span></span>
<span data-ttu-id="66f81-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="66f81-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66f81-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66f81-133">CommonParameters</span></span>
<span data-ttu-id="66f81-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66f81-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66f81-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66f81-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66f81-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66f81-136">INPUTS</span></span>

### <span data-ttu-id="66f81-137">Arskasa</span><span class="sxs-lookup"><span data-stu-id="66f81-137">ARSVault</span></span>
<span data-ttu-id="66f81-138">Parametre ' kasa ', ardışık düzenin ' Arskasa ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="66f81-138">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="66f81-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66f81-139">OUTPUTS</span></span>

### <span data-ttu-id="66f81-140">Microsoft. Azure. Commands. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="66f81-140">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="66f81-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66f81-141">NOTES</span></span>

## <span data-ttu-id="66f81-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66f81-142">RELATED LINKS</span></span>

[<span data-ttu-id="66f81-143">Get-Azurermrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="66f81-143">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="66f81-144">Yeni-Azurermrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="66f81-144">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="66f81-145">Remove-Azurermrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="66f81-145">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


