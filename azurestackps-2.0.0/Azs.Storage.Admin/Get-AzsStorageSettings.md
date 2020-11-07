---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 3ad33f83a4e8f96124682bbb189f210f813ead25
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935975"
---
# <span data-ttu-id="037e4-101">Get-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="037e4-101">Get-AzsStorageSettings</span></span>

## <span data-ttu-id="037e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="037e4-102">SYNOPSIS</span></span>
<span data-ttu-id="037e4-103">Depolama kaynak sağlayıcısı ayarlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="037e4-103">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="037e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="037e4-104">SYNTAX</span></span>

```
Get-AzsStorageSettings [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="037e4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="037e4-105">DESCRIPTION</span></span>
<span data-ttu-id="037e4-106">Depolama kaynak sağlayıcısı ayarlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="037e4-106">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="037e4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="037e4-107">EXAMPLES</span></span>

### <span data-ttu-id="037e4-108">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="037e4-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageSettings
```

<span data-ttu-id="037e4-109">Depolama ayarlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="037e4-109">Get the storage settings.</span></span>

## <span data-ttu-id="037e4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="037e4-110">PARAMETERS</span></span>

### <span data-ttu-id="037e4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="037e4-111">-DefaultProfile</span></span>
<span data-ttu-id="037e4-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="037e4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="037e4-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="037e4-113">-Location</span></span>
<span data-ttu-id="037e4-114">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="037e4-114">Resource location.</span></span>

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

### <span data-ttu-id="037e4-115">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="037e4-115">-SubscriptionId</span></span>
<span data-ttu-id="037e4-116">Abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="037e4-116">Subscription Id.</span></span>

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

### <span data-ttu-id="037e4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="037e4-117">CommonParameters</span></span>
<span data-ttu-id="037e4-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="037e4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="037e4-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="037e4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="037e4-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="037e4-120">INPUTS</span></span>

## <span data-ttu-id="037e4-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="037e4-121">OUTPUTS</span></span>

### <span data-ttu-id="037e4-122">Microsoft. Azure. PowerShell. cmdlet. StorageAdmin. modeller. Api201908Preview. ısettings</span><span class="sxs-lookup"><span data-stu-id="037e4-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="037e4-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="037e4-123">NOTES</span></span>

## <span data-ttu-id="037e4-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="037e4-124">RELATED LINKS</span></span>

