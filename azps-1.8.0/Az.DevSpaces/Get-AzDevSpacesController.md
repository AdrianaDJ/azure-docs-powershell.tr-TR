---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: 7cc4c61073b0b196faca8d95bd5153abe2587ee7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760965"
---
# <span data-ttu-id="52a8a-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="52a8a-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="52a8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52a8a-102">SYNOPSIS</span></span>
<span data-ttu-id="52a8a-103">Azure DevSpaces denetleyicisini alın veya listeleyin.</span><span class="sxs-lookup"><span data-stu-id="52a8a-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="52a8a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52a8a-104">SYNTAX</span></span>

### <span data-ttu-id="52a8a-105">ListDevSpacesControllerParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="52a8a-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="52a8a-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="52a8a-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52a8a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="52a8a-107">DESCRIPTION</span></span>
<span data-ttu-id="52a8a-108">Azure DevSpaces denetleyicisini alın veya listeleyin.</span><span class="sxs-lookup"><span data-stu-id="52a8a-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="52a8a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52a8a-109">EXAMPLES</span></span>

### <span data-ttu-id="52a8a-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="52a8a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="52a8a-111">Bir abonelikteki tüm denetleyicileri listeleyin.</span><span class="sxs-lookup"><span data-stu-id="52a8a-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="52a8a-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="52a8a-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="52a8a-113">Aboneliğe bir DevSpaces denetleyicileri edinin.</span><span class="sxs-lookup"><span data-stu-id="52a8a-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="52a8a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52a8a-114">PARAMETERS</span></span>

### <span data-ttu-id="52a8a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52a8a-115">-DefaultProfile</span></span>
<span data-ttu-id="52a8a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="52a8a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52a8a-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="52a8a-117">-Name</span></span>
<span data-ttu-id="52a8a-118">DevSpaces denetleyici adı.</span><span class="sxs-lookup"><span data-stu-id="52a8a-118">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a8a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52a8a-119">-ResourceGroupName</span></span>
<span data-ttu-id="52a8a-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="52a8a-120">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ListDevSpacesControllerParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a8a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a8a-121">CommonParameters</span></span>
<span data-ttu-id="52a8a-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52a8a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a8a-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52a8a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a8a-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52a8a-124">INPUTS</span></span>

### <span data-ttu-id="52a8a-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="52a8a-125">None</span></span>

## <span data-ttu-id="52a8a-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52a8a-126">OUTPUTS</span></span>

### <span data-ttu-id="52a8a-127">Microsoft. Azure. Commands. DevSpaces. modeller. PSController</span><span class="sxs-lookup"><span data-stu-id="52a8a-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="52a8a-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52a8a-128">NOTES</span></span>

## <span data-ttu-id="52a8a-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52a8a-129">RELATED LINKS</span></span>
