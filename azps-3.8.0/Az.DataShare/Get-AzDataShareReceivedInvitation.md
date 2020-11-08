---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 18cd37f1e24851720299a647a30323f9379bea6a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096647"
---
# <span data-ttu-id="96b08-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="96b08-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="96b08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96b08-102">SYNOPSIS</span></span>
<span data-ttu-id="96b08-103">Tüketici davetleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="96b08-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="96b08-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="96b08-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96b08-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="96b08-105">DESCRIPTION</span></span>
<span data-ttu-id="96b08-106">**Get-Azdatasharerecevedınvitation** cmdlet 'i, tüketicinin sahip olduğu tüm davetlerin hakkında bilgi receieved.</span><span class="sxs-lookup"><span data-stu-id="96b08-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="96b08-107">Konum veya davet kimliği sağlarsanız, bu cmdlet belirli bir konumda veya davet kimliğine sahip olan davet hakkında bilgi sağlar. Aksi takdirde tüketiciye gönderilen davetlerin listesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="96b08-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="96b08-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="96b08-108">EXAMPLES</span></span>

### <span data-ttu-id="96b08-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="96b08-109">Example 1</span></span>
```
PS C:\> Get-AzDataShareReceivedInvitation -location "westus"

DataSetCount      : 3
InvitationId      : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus  : Pending
Location          : westus
RespondedAt       :
Sender            : adsprovider@microsoft.com
SenderCompanyName : ADS Test
SentAt            : 7/8/2019 10:47:10 PM
ShareName         : AdsShare
Description       : Some description
Terms             : Some terms of use
Id                : /providers/Microsoft.DataShare/consumerInvitations/167e06ff-567f-4bc7-be0c-645a6de710f3
Name              : AdsInvitation
Type              : Microsoft.DataShare/consumerInvitations
```

<span data-ttu-id="96b08-110">Bu commantüketici davetleri hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="96b08-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="96b08-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="96b08-111">PARAMETERS</span></span>

### <span data-ttu-id="96b08-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96b08-112">-DefaultProfile</span></span>
<span data-ttu-id="96b08-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="96b08-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96b08-114">-Davetsiz</span><span class="sxs-lookup"><span data-stu-id="96b08-114">-InvitationId</span></span>
<span data-ttu-id="96b08-115">Azure dataShare davet kimliği.</span><span class="sxs-lookup"><span data-stu-id="96b08-115">Azure dataShare invitation id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96b08-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="96b08-116">-Location</span></span>
<span data-ttu-id="96b08-117">Azure veri paylaşımı davet konumu.</span><span class="sxs-lookup"><span data-stu-id="96b08-117">Azure data share invitation location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96b08-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96b08-118">CommonParameters</span></span>
<span data-ttu-id="96b08-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="96b08-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96b08-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96b08-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96b08-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="96b08-121">INPUTS</span></span>

### <span data-ttu-id="96b08-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="96b08-122">None</span></span>

## <span data-ttu-id="96b08-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="96b08-123">OUTPUTS</span></span>

### <span data-ttu-id="96b08-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDAtapaylaşımı</span><span class="sxs-lookup"><span data-stu-id="96b08-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="96b08-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="96b08-125">NOTES</span></span>

## <span data-ttu-id="96b08-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="96b08-126">RELATED LINKS</span></span>
