---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 939b50f6725497bb28ea333f13c04c6281f34611
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320357"
---
# <span data-ttu-id="cb2fc-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="cb2fc-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="cb2fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb2fc-102">SYNOPSIS</span></span>
<span data-ttu-id="cb2fc-103">Tüketici davetleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="cb2fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb2fc-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb2fc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb2fc-105">DESCRIPTION</span></span>
<span data-ttu-id="cb2fc-106">**Get-Azdatasharerecevedınvitation** cmdlet 'i, tüketicinin sahip olduğu tüm davetlerin hakkında bilgi receieved.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="cb2fc-107">Konum veya davet kimliği sağlarsanız, bu cmdlet belirli bir konumda veya davet kimliğine sahip olan davet hakkında bilgi sağlar. Aksi takdirde tüketiciye gönderilen davetlerin listesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="cb2fc-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb2fc-108">EXAMPLES</span></span>

### <span data-ttu-id="cb2fc-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cb2fc-109">Example 1</span></span>
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

<span data-ttu-id="cb2fc-110">Bu commantüketici davetleri hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="cb2fc-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb2fc-111">PARAMETERS</span></span>

### <span data-ttu-id="cb2fc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb2fc-112">-DefaultProfile</span></span>
<span data-ttu-id="cb2fc-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb2fc-114">-Davetsiz</span><span class="sxs-lookup"><span data-stu-id="cb2fc-114">-InvitationId</span></span>
<span data-ttu-id="cb2fc-115">Azure dataShare davet kimliği.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-115">Azure dataShare invitation id.</span></span>

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

### <span data-ttu-id="cb2fc-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="cb2fc-116">-Location</span></span>
<span data-ttu-id="cb2fc-117">Azure veri paylaşımı davet konumu.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-117">Azure data share invitation location.</span></span>

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

### <span data-ttu-id="cb2fc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb2fc-118">CommonParameters</span></span>
<span data-ttu-id="cb2fc-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb2fc-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb2fc-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb2fc-121">INPUTS</span></span>

### <span data-ttu-id="cb2fc-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cb2fc-122">None</span></span>

## <span data-ttu-id="cb2fc-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb2fc-123">OUTPUTS</span></span>

### <span data-ttu-id="cb2fc-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDAtapaylaşımı</span><span class="sxs-lookup"><span data-stu-id="cb2fc-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="cb2fc-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb2fc-125">NOTES</span></span>

## <span data-ttu-id="cb2fc-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb2fc-126">RELATED LINKS</span></span>
