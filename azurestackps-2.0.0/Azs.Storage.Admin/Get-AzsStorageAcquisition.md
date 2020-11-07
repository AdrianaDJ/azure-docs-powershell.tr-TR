---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstorageacquisition
schema: 2.0.0
ms.openlocfilehash: 098c268d3894d85efe0e17618b5d7ec46b82b0f2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935976"
---
# <span data-ttu-id="61597-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="61597-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="61597-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61597-102">SYNOPSIS</span></span>
<span data-ttu-id="61597-103">BLOB alma listesi listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="61597-103">Returns a list of BLOB acquisitions.</span></span>

## <span data-ttu-id="61597-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61597-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="61597-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="61597-105">DESCRIPTION</span></span>
<span data-ttu-id="61597-106">BLOB alma listesi listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="61597-106">Returns a list of BLOB acquisitions.</span></span>

## <span data-ttu-id="61597-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61597-107">EXAMPLES</span></span>

### <span data-ttu-id="61597-108">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="61597-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageAcquisition
```

<span data-ttu-id="61597-109">Blob alma işlemleri listesini alın.</span><span class="sxs-lookup"><span data-stu-id="61597-109">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="61597-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61597-110">PARAMETERS</span></span>

### <span data-ttu-id="61597-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61597-111">-DefaultProfile</span></span>
<span data-ttu-id="61597-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="61597-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="61597-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="61597-113">-Location</span></span>
<span data-ttu-id="61597-114">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="61597-114">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="61597-115">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="61597-115">-SubscriptionId</span></span>
<span data-ttu-id="61597-116">Abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="61597-116">Subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="61597-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61597-117">CommonParameters</span></span>
<span data-ttu-id="61597-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61597-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61597-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="61597-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61597-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61597-120">INPUTS</span></span>

## <span data-ttu-id="61597-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61597-121">OUTPUTS</span></span>

### <span data-ttu-id="61597-122">Microsoft. Azure. PowerShell. cmdlet. StorageAdmin. modeller. Api201908Preview. ıalımı</span><span class="sxs-lookup"><span data-stu-id="61597-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IAcquisition</span></span>



## <span data-ttu-id="61597-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61597-123">NOTES</span></span>

## <span data-ttu-id="61597-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61597-124">RELATED LINKS</span></span>

