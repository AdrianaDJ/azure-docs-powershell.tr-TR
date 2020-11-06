---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 070DA86E-9EA4-4777-9D53-64B58B4401B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 42863e0dbf6982ced1f77f916c97ed4fc19d6979
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594168"
---
# <span data-ttu-id="910c3-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="910c3-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="910c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="910c3-102">SYNOPSIS</span></span>
<span data-ttu-id="910c3-103">Site Recovery kasa ayarları dosyasını içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="910c3-103">Imports a Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="910c3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="910c3-104">SYNTAX</span></span>

```
Import-AzureRmSiteRecoveryVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="910c3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="910c3-105">DESCRIPTION</span></span>
<span data-ttu-id="910c3-106">**Import-AzureRmSiteRecoveryVaultSettingsFile** cmdlet 'i, geçerli oturumdaki sonraki site kurtarma işlemleri için kasa bağlamını ayarlamak üzere bir Azure Site Recovery kasa ayarları dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="910c3-106">The **Import-AzureRmSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="910c3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="910c3-107">EXAMPLES</span></span>

## <span data-ttu-id="910c3-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="910c3-108">PARAMETERS</span></span>

### <span data-ttu-id="910c3-109">-Yol</span><span class="sxs-lookup"><span data-stu-id="910c3-109">-Path</span></span>
<span data-ttu-id="910c3-110">Site Recovery kasa ayarları dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="910c3-110">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="910c3-111">Bu dosya, Site Recovery kasa portalından indirilebilir ve yerel olarak depolanabilir.</span><span class="sxs-lookup"><span data-stu-id="910c3-111">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

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

### <span data-ttu-id="910c3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="910c3-112">-DefaultProfile</span></span>
<span data-ttu-id="910c3-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="910c3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="910c3-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="910c3-114">CommonParameters</span></span>
<span data-ttu-id="910c3-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="910c3-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="910c3-116">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="910c3-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="910c3-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="910c3-117">INPUTS</span></span>

## <span data-ttu-id="910c3-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="910c3-118">OUTPUTS</span></span>

### <span data-ttu-id="910c3-119">Microsoft. Azure. Commands. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="910c3-119">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="910c3-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="910c3-120">NOTES</span></span>

## <span data-ttu-id="910c3-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="910c3-121">RELATED LINKS</span></span>

[<span data-ttu-id="910c3-122">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="910c3-122">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureRmSiteRecoveryVaultSettingsFile.md)
