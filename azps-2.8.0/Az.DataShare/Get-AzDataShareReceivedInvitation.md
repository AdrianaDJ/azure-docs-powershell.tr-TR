---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 7191d7b1f24909676a8b854a2b7836533401f89a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752212"
---
# <span data-ttu-id="a8a4d-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="a8a4d-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="a8a4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="a8a4d-103">Tüketici davetleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="a8a4d-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="a8a4d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a8a4d-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8a4d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a8a4d-105">DESCRIPTION</span></span>
<span data-ttu-id="a8a4d-106">**Get-Azdatasharerecevedınvitation** cmdlet 'i, tüketicinin sahip olduğu tüm davetlerin hakkında bilgi receieved.</span><span class="sxs-lookup"><span data-stu-id="a8a4d-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="a8a4d-107">Konum veya davet kimliği sağlarsanız, bu cmdlet belirli bir konumda veya davet kimliğine sahip olan davet hakkında bilgi sağlar. Aksi takdirde tüketiciye gönderilen davetlerin listesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="a8a4d-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="a8a4d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a8a4d-108">EXAMPLES</span></span>

### <span data-ttu-id="a8a4d-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a8a4d-109">Example 1</span></span>
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

<span data-ttu-id="a8a4d-110">Bu commantüketici davetleri hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a8a4d-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="a8a4d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a8a4d-111">PARAMETERS</span></span>

### <span data-ttu-id="a8a4d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8a4d-112">-DefaultProfile</span></span>
<span data-ttu-id="a8a4d-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a8a4d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8a4d-114">-Davetsiz</span><span class="sxs-lookup"><span data-stu-id="a8a4d-114">-InvitationId</span></span>
<span data-ttu-id="a8a4d-115">Azure dataShare davet kimliği.</span><span class="sxs-lookup"><span data-stu-id="a8a4d-115">Azure dataShare invitation id.</span></span>

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

### <span data-ttu-id="a8a4d-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="a8a4d-116">-Location</span></span>
<span data-ttu-id="a8a4d-117">Azure veri paylaşımı davet konumu.</span><span class="sxs-lookup"><span data-stu-id="a8a4d-117">Azure data share invitation location.</span></span>

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

### <span data-ttu-id="a8a4d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8a4d-118">CommonParameters</span></span>
<span data-ttu-id="a8a4d-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a8a4d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8a4d-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8a4d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8a4d-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a8a4d-121">INPUTS</span></span>

### <span data-ttu-id="a8a4d-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a8a4d-122">None</span></span>

## <span data-ttu-id="a8a4d-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a8a4d-123">OUTPUTS</span></span>

### <span data-ttu-id="a8a4d-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDAtapaylaşımı</span><span class="sxs-lookup"><span data-stu-id="a8a4d-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="a8a4d-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a8a4d-125">NOTES</span></span>

## <span data-ttu-id="a8a4d-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a8a4d-126">RELATED LINKS</span></span>
