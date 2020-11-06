---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: AD76C752-2070-449D-BF4F-B4260B05AB02
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: 6afb5be21f1000cf2e18cd8a4b9e1dfa4f159ee0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592535"
---
# <span data-ttu-id="acefe-101">Update-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="acefe-101">Update-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="acefe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acefe-102">SYNOPSIS</span></span>
<span data-ttu-id="acefe-103">Site kurtarma sunucusunu yeniler.</span><span class="sxs-lookup"><span data-stu-id="acefe-103">Refreshes a Site Recovery server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acefe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="acefe-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServer -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="acefe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="acefe-105">DESCRIPTION</span></span>
<span data-ttu-id="acefe-106">**Update-AzureRmSiteRecoveryServer** cmdlet 'ı bir Azure Site Recovery sunucusunu yeniler.</span><span class="sxs-lookup"><span data-stu-id="acefe-106">The **Update-AzureRmSiteRecoveryServer** cmdlet refreshes an Azure Site Recovery server.</span></span>

## <span data-ttu-id="acefe-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="acefe-107">EXAMPLES</span></span>

## <span data-ttu-id="acefe-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="acefe-108">PARAMETERS</span></span>

### <span data-ttu-id="acefe-109">-Sunucu</span><span class="sxs-lookup"><span data-stu-id="acefe-109">-Server</span></span>
<span data-ttu-id="acefe-110">Bu cmdlet 'in güncelleştirdiği site kurtarma sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="acefe-110">Specifies the Site Recovery server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acefe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acefe-111">-DefaultProfile</span></span>
<span data-ttu-id="acefe-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="acefe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acefe-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acefe-113">CommonParameters</span></span>
<span data-ttu-id="acefe-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="acefe-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acefe-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acefe-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acefe-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="acefe-116">INPUTS</span></span>

### <span data-ttu-id="acefe-117">ASRServer</span><span class="sxs-lookup"><span data-stu-id="acefe-117">ASRServer</span></span>
<span data-ttu-id="acefe-118">' Server ' parametresi ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="acefe-118">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="acefe-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="acefe-119">OUTPUTS</span></span>

## <span data-ttu-id="acefe-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="acefe-120">NOTES</span></span>

## <span data-ttu-id="acefe-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="acefe-121">RELATED LINKS</span></span>

[<span data-ttu-id="acefe-122">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="acefe-122">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="acefe-123">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="acefe-123">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
