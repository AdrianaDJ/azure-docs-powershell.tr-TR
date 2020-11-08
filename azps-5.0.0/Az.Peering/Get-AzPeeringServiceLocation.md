---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservicelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
ms.openlocfilehash: 6f869cee7258c38e941ca8fbb7c8ac31b47171af
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276372"
---
# <span data-ttu-id="2b3d7-101">Get-AzPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="2b3d7-101">Get-AzPeeringServiceLocation</span></span>

## <span data-ttu-id="2b3d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b3d7-102">SYNOPSIS</span></span>
<span data-ttu-id="2b3d7-103">Microsoft tarafından sunulan eşleme hizmeti konumlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="2b3d7-103">Gets a list of peering service locations offered by Microsoft.</span></span>

## <span data-ttu-id="2b3d7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2b3d7-104">SYNTAX</span></span>

```
Get-AzPeeringServiceLocation [-Country <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b3d7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b3d7-105">DESCRIPTION</span></span>
<span data-ttu-id="2b3d7-106">Liste eşleme konumları.</span><span class="sxs-lookup"><span data-stu-id="2b3d7-106">List peering locations.</span></span>

## <span data-ttu-id="2b3d7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2b3d7-107">EXAMPLES</span></span>

### <span data-ttu-id="2b3d7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2b3d7-108">Example 1</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States" | Where-Object { $_.State -match "Washington"}

Country     : United States
State       : Washington
AzureRegion : West US
Name        : Washington
Id          :
Type        : Microsoft.Peering/peeringServiceLocations
```

<span data-ttu-id="2b3d7-109">Washington için eşleme konumlarını alır.</span><span class="sxs-lookup"><span data-stu-id="2b3d7-109">Retrieves the peering locations for washington.</span></span>

### <span data-ttu-id="2b3d7-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2b3d7-110">Example 2</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States"

Country     : United States
State       : Alabama
AzureRegion : East US
Name        : Alabama
Id          :
Type        : Microsoft.Peering/peeringServiceLocations

Country     : United States
State       : Arizona
AzureRegion : West US
Name        : Arizona
Id          :
Type        : Microsoft.Peering/peeringServiceLocations

...
```

<span data-ttu-id="2b3d7-111">Washington için eşleme konumlarını alır.</span><span class="sxs-lookup"><span data-stu-id="2b3d7-111">Retrieves the peering locations for washington.</span></span>

## <span data-ttu-id="2b3d7-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2b3d7-112">PARAMETERS</span></span>

### <span data-ttu-id="2b3d7-113">-Ülke</span><span class="sxs-lookup"><span data-stu-id="2b3d7-113">-Country</span></span>
<span data-ttu-id="2b3d7-114">Ülke filtresi</span><span class="sxs-lookup"><span data-stu-id="2b3d7-114">The country filter</span></span>

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

### <span data-ttu-id="2b3d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b3d7-115">-DefaultProfile</span></span>
<span data-ttu-id="2b3d7-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2b3d7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b3d7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b3d7-117">CommonParameters</span></span>
<span data-ttu-id="2b3d7-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2b3d7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b3d7-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2b3d7-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b3d7-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2b3d7-120">INPUTS</span></span>

### <span data-ttu-id="2b3d7-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2b3d7-121">None</span></span>

## <span data-ttu-id="2b3d7-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2b3d7-122">OUTPUTS</span></span>

### <span data-ttu-id="2b3d7-123">Microsoft. Azure. PowerShell. cmdlet. eşleme. modeller. PSPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="2b3d7-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="2b3d7-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2b3d7-124">NOTES</span></span>

## <span data-ttu-id="2b3d7-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2b3d7-125">RELATED LINKS</span></span>
