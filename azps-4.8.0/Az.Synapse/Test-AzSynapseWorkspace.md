---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: b3dd32ec177aaa38e8fbb1f66559592f84905f2d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268934"
---
# <span data-ttu-id="2a2d7-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2a2d7-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="2a2d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a2d7-102">SYNOPSIS</span></span>
<span data-ttu-id="2a2d7-103">SYNAPSE Analytics çalışma alanının varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="2a2d7-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="2a2d7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a2d7-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a2d7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a2d7-105">DESCRIPTION</span></span>
<span data-ttu-id="2a2d7-106">**Test-AzSynapseWorkspace** cmdlet 'ı SYNAPSE Analytics çalışma alanı varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="2a2d7-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="2a2d7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a2d7-107">EXAMPLES</span></span>

### <span data-ttu-id="2a2d7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2a2d7-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="2a2d7-109">Bu komut, SYNAPSE Analytics çalışma alanının varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="2a2d7-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="2a2d7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a2d7-110">PARAMETERS</span></span>

### <span data-ttu-id="2a2d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a2d7-111">-DefaultProfile</span></span>
<span data-ttu-id="2a2d7-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2a2d7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a2d7-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="2a2d7-113">-Name</span></span>
<span data-ttu-id="2a2d7-114">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="2a2d7-114">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a2d7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a2d7-115">-ResourceGroupName</span></span>
<span data-ttu-id="2a2d7-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2a2d7-116">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a2d7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a2d7-117">CommonParameters</span></span>
<span data-ttu-id="2a2d7-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a2d7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a2d7-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2a2d7-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a2d7-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a2d7-120">INPUTS</span></span>

### <span data-ttu-id="2a2d7-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2a2d7-121">None</span></span>

## <span data-ttu-id="2a2d7-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a2d7-122">OUTPUTS</span></span>

### <span data-ttu-id="2a2d7-123">System. Object</span><span class="sxs-lookup"><span data-stu-id="2a2d7-123">System.Object</span></span>
## <span data-ttu-id="2a2d7-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a2d7-124">NOTES</span></span>

## <span data-ttu-id="2a2d7-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a2d7-125">RELATED LINKS</span></span>
