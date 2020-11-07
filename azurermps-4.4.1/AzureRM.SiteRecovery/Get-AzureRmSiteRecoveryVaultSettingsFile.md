---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 9595E785-6DBF-433C-83B3-8506A3B49B13
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 242dfd46b179d1e7d55613d938eddf5b691da6c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764513"
---
# <span data-ttu-id="f64dd-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f64dd-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="f64dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f64dd-102">SYNOPSIS</span></span>
<span data-ttu-id="f64dd-103">Site Recovery kasa ayarları dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="f64dd-103">Gets the Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f64dd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f64dd-104">SYNTAX</span></span>

### <span data-ttu-id="f64dd-105">ByParam (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f64dd-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f64dd-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="f64dd-106">Default</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f64dd-107">Forsıte</span><span class="sxs-lookup"><span data-stu-id="f64dd-107">ForSite</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> -SiteIdentifier <String> -SiteFriendlyName <String>
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f64dd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f64dd-108">DESCRIPTION</span></span>
<span data-ttu-id="f64dd-109">**Get-AzureRmSiteRecoveryVaultSettingsFile** cmdlet 'ı bir Azure Site Recovery Kasası için ayarlar dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="f64dd-109">The **Get-AzureRmSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="f64dd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f64dd-110">EXAMPLES</span></span>

## <span data-ttu-id="f64dd-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f64dd-111">PARAMETERS</span></span>

### <span data-ttu-id="f64dd-112">-Yol</span><span class="sxs-lookup"><span data-stu-id="f64dd-112">-Path</span></span>
<span data-ttu-id="f64dd-113">Site Recovery kasa ayarları dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f64dd-113">Specifies the path to the Site Recovery vault settings file.</span></span>
<span data-ttu-id="f64dd-114">Bu dosyayı yerel olarak depolamak için, komut tamamlandığında site kurtarma Kasası portalında indirin.</span><span class="sxs-lookup"><span data-stu-id="f64dd-114">To store this file locally, download it from the Site Recovery vault portal once the command completes.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, ForSite
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f64dd-115">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f64dd-115">-SiteFriendlyName</span></span>
<span data-ttu-id="f64dd-116">Site bir Hyper-V sitesi olduğunda kasanın kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f64dd-116">Specifies the site friendly name for the vault when the site is a Hyper-V site.</span></span>

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

### <span data-ttu-id="f64dd-117">-Sitetanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="f64dd-117">-SiteIdentifier</span></span>
<span data-ttu-id="f64dd-118">Site bir Hyper-V sitesi olduğunda kasaya ait site tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f64dd-118">Specifies the site identifier for the vault when the site is a Hyper-V site.</span></span>

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

### <span data-ttu-id="f64dd-119">-Kasa</span><span class="sxs-lookup"><span data-stu-id="f64dd-119">-Vault</span></span>
<span data-ttu-id="f64dd-120">Sitenin kasa nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f64dd-120">Specifies the vault object for the site.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: Default, ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f64dd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f64dd-121">-DefaultProfile</span></span>
<span data-ttu-id="f64dd-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f64dd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f64dd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f64dd-123">CommonParameters</span></span>
<span data-ttu-id="f64dd-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f64dd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f64dd-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f64dd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f64dd-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f64dd-126">INPUTS</span></span>

### <span data-ttu-id="f64dd-127">Asrkasa</span><span class="sxs-lookup"><span data-stu-id="f64dd-127">ASRVault</span></span>
<span data-ttu-id="f64dd-128">Parametre ' kasa ', ardışık düzenin ' Asrkasa ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="f64dd-128">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="f64dd-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f64dd-129">OUTPUTS</span></span>

### <span data-ttu-id="f64dd-130">Microsoft. Azure. Commands. SiteRecovery. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="f64dd-130">Microsoft.Azure.Commands.SiteRecovery.VaultSettingsFilePath</span></span>

## <span data-ttu-id="f64dd-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f64dd-131">NOTES</span></span>

## <span data-ttu-id="f64dd-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f64dd-132">RELATED LINKS</span></span>

[<span data-ttu-id="f64dd-133">İçeri aktarma-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f64dd-133">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureRmSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="f64dd-134">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="f64dd-134">Set-AzureRmSiteRecoveryVaultSettings</span></span>](./Set-AzureRmSiteRecoveryVaultSettings.md)
