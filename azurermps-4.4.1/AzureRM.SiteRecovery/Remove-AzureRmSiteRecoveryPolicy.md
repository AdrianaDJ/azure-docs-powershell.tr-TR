---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: C4C624DB-BBE8-4F94-BDC6-C012482F7271
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 3b01e089271cc131af5a4258c46836a87104ef62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762683"
---
# <span data-ttu-id="aa2b7-101">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="aa2b7-101">Remove-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="aa2b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa2b7-102">SYNOPSIS</span></span>
<span data-ttu-id="aa2b7-103">Site kurtarma çoğaltma ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-103">Removes a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa2b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aa2b7-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa2b7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="aa2b7-105">DESCRIPTION</span></span>
<span data-ttu-id="aa2b7-106">**Remove-AzureRMSiteRecoveryPolicy** cmdlet 'ı bir Azure Site Recovery çoğaltma ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-106">The **Remove-AzureRMSiteRecoveryPolicy** cmdlet removes an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="aa2b7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aa2b7-107">EXAMPLES</span></span>

## <span data-ttu-id="aa2b7-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aa2b7-108">PARAMETERS</span></span>

### <span data-ttu-id="aa2b7-109">-İlke</span><span class="sxs-lookup"><span data-stu-id="aa2b7-109">-Policy</span></span>
<span data-ttu-id="aa2b7-110">Site kurtarma ilkesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-110">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa2b7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa2b7-111">-DefaultProfile</span></span>
<span data-ttu-id="aa2b7-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa2b7-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa2b7-113">CommonParameters</span></span>
<span data-ttu-id="aa2b7-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa2b7-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa2b7-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa2b7-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aa2b7-116">INPUTS</span></span>

### <span data-ttu-id="aa2b7-117">Asrilkesi</span><span class="sxs-lookup"><span data-stu-id="aa2b7-117">ASRPolicy</span></span>
<span data-ttu-id="aa2b7-118">Parametre ' Ilke ', ardışık düzenin ' ASRPolicy ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="aa2b7-118">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="aa2b7-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aa2b7-119">OUTPUTS</span></span>

## <span data-ttu-id="aa2b7-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aa2b7-120">NOTES</span></span>

## <span data-ttu-id="aa2b7-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aa2b7-121">RELATED LINKS</span></span>

[<span data-ttu-id="aa2b7-122">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="aa2b7-122">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="aa2b7-123">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="aa2b7-123">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)
