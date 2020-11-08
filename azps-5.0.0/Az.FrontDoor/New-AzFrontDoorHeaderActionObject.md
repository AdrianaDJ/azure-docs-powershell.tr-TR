---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: e718fbf4c46c69e5076ab95311aedb54132b604f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277417"
---
# <span data-ttu-id="c43c3-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="c43c3-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="c43c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c43c3-102">SYNOPSIS</span></span>
<span data-ttu-id="c43c3-103">PSHeaderAction nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c43c3-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="c43c3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c43c3-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c43c3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c43c3-105">DESCRIPTION</span></span>
<span data-ttu-id="c43c3-106">PSRulesEngineAction nesnesinin oluşturulması için PSHeaderAction nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c43c3-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="c43c3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c43c3-107">EXAMPLES</span></span>

### <span data-ttu-id="c43c3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c43c3-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="c43c3-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c43c3-109">PARAMETERS</span></span>

### <span data-ttu-id="c43c3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c43c3-110">-DefaultProfile</span></span>
<span data-ttu-id="c43c3-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c43c3-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c43c3-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="c43c3-112">-HeaderActionType</span></span>
<span data-ttu-id="c43c3-113">Üstbilgiye uygulanacak düzenleme türü.</span><span class="sxs-lookup"><span data-stu-id="c43c3-113">Which type of manipulation to apply to the header.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderActionType
Parameter Sets: (All)
Aliases:
Accepted values: Append, Delete, Overwrite

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c43c3-114">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="c43c3-114">-HeaderName</span></span>
<span data-ttu-id="c43c3-115">Bu eylemin uygulanacağı başlığın adı.</span><span class="sxs-lookup"><span data-stu-id="c43c3-115">The name of the header this action will apply to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c43c3-116">-Değer</span><span class="sxs-lookup"><span data-stu-id="c43c3-116">-Value</span></span>
<span data-ttu-id="c43c3-117">Belirtilen üst bilgi adını ile güncelleştirilecek değer.</span><span class="sxs-lookup"><span data-stu-id="c43c3-117">The value to update the given header name with.</span></span>
<span data-ttu-id="c43c3-118">ActionType Delete ise bu değer kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="c43c3-118">This value is not used if the actionType is Delete.</span></span>

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

### <span data-ttu-id="c43c3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c43c3-119">CommonParameters</span></span>
<span data-ttu-id="c43c3-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c43c3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c43c3-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c43c3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c43c3-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c43c3-122">INPUTS</span></span>

### <span data-ttu-id="c43c3-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c43c3-123">None</span></span>

## <span data-ttu-id="c43c3-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c43c3-124">OUTPUTS</span></span>

### <span data-ttu-id="c43c3-125">Microsoft. Azure. Commands. Frontkapısı. modeller. PSHeaderAction</span><span class="sxs-lookup"><span data-stu-id="c43c3-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="c43c3-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c43c3-126">NOTES</span></span>

## <span data-ttu-id="c43c3-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c43c3-127">RELATED LINKS</span></span>
