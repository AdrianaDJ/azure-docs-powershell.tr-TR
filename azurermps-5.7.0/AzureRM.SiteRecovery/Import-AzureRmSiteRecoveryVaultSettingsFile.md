---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 070DA86E-9EA4-4777-9D53-64B58B4401B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/import-azurermsiterecoveryvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 11233414250377331f75e3e8b69f262a0f3a0537
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593391"
---
# <span data-ttu-id="7641c-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="7641c-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="7641c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7641c-102">SYNOPSIS</span></span>
<span data-ttu-id="7641c-103">Site Recovery kasa ayarları dosyasını içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="7641c-103">Imports a Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7641c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7641c-104">SYNTAX</span></span>

```
Import-AzureRmSiteRecoveryVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7641c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7641c-105">DESCRIPTION</span></span>
<span data-ttu-id="7641c-106">**Import-AzureRmSiteRecoveryVaultSettingsFile** cmdlet 'i, geçerli oturumdaki sonraki site kurtarma işlemleri için kasa bağlamını ayarlamak üzere bir Azure Site Recovery kasa ayarları dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="7641c-106">The **Import-AzureRmSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="7641c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7641c-107">EXAMPLES</span></span>

## <span data-ttu-id="7641c-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7641c-108">PARAMETERS</span></span>

### <span data-ttu-id="7641c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7641c-109">-DefaultProfile</span></span>
<span data-ttu-id="7641c-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7641c-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7641c-111">-Yol</span><span class="sxs-lookup"><span data-stu-id="7641c-111">-Path</span></span>
<span data-ttu-id="7641c-112">Site Recovery kasa ayarları dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7641c-112">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="7641c-113">Bu dosya, Site Recovery kasa portalından indirilebilir ve yerel olarak depolanabilir.</span><span class="sxs-lookup"><span data-stu-id="7641c-113">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

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

### <span data-ttu-id="7641c-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7641c-114">CommonParameters</span></span>
<span data-ttu-id="7641c-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7641c-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7641c-116">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7641c-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7641c-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7641c-117">INPUTS</span></span>

### <span data-ttu-id="7641c-118">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7641c-118">None</span></span>
<span data-ttu-id="7641c-119">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="7641c-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7641c-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7641c-120">OUTPUTS</span></span>

### <span data-ttu-id="7641c-121">Microsoft. Azure. Commands. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="7641c-121">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="7641c-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7641c-122">NOTES</span></span>

## <span data-ttu-id="7641c-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7641c-123">RELATED LINKS</span></span>

[<span data-ttu-id="7641c-124">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="7641c-124">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureRmSiteRecoveryVaultSettingsFile.md)
