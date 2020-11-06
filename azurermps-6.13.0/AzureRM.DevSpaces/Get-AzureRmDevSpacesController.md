---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/get-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Get-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Get-AzureRmDevSpacesController.md
ms.openlocfilehash: d0140af9d5345e9f3f68c212ae43403fc0f64280
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589563"
---
# <span data-ttu-id="1e82c-101">Get-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="1e82c-101">Get-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="1e82c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e82c-102">SYNOPSIS</span></span>
<span data-ttu-id="1e82c-103">Azure DevSpaces denetleyicisini alın veya listeleyin.</span><span class="sxs-lookup"><span data-stu-id="1e82c-103">Get or list Azure DevSpaces controller.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e82c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e82c-104">SYNTAX</span></span>

### <span data-ttu-id="1e82c-105">ListDevSpacesControllerParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1e82c-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzureRmDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e82c-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e82c-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e82c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e82c-107">DESCRIPTION</span></span>
<span data-ttu-id="1e82c-108">Azure DevSpaces denetleyicisini alın veya listeleyin.</span><span class="sxs-lookup"><span data-stu-id="1e82c-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="1e82c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e82c-109">EXAMPLES</span></span>

### <span data-ttu-id="1e82c-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1e82c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="1e82c-111">Bir abonelikteki tüm denetleyicileri listeleyin.</span><span class="sxs-lookup"><span data-stu-id="1e82c-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="1e82c-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1e82c-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="1e82c-113">Aboneliğe bir DevSpaces denetleyicileri edinin.</span><span class="sxs-lookup"><span data-stu-id="1e82c-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="1e82c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e82c-114">PARAMETERS</span></span>

### <span data-ttu-id="1e82c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e82c-115">-DefaultProfile</span></span>
<span data-ttu-id="1e82c-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1e82c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e82c-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="1e82c-117">-Name</span></span>
<span data-ttu-id="1e82c-118">DevSpaces denetleyici adı.</span><span class="sxs-lookup"><span data-stu-id="1e82c-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="1e82c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e82c-119">-ResourceGroupName</span></span>
<span data-ttu-id="1e82c-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="1e82c-120">Resource group name</span></span>

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

### <span data-ttu-id="1e82c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e82c-121">CommonParameters</span></span>
<span data-ttu-id="1e82c-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e82c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e82c-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e82c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e82c-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e82c-124">INPUTS</span></span>

### <span data-ttu-id="1e82c-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1e82c-125">None</span></span>

## <span data-ttu-id="1e82c-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e82c-126">OUTPUTS</span></span>

### <span data-ttu-id="1e82c-127">Microsoft. Azure. Commands. DevSpaces. modeller. PSController</span><span class="sxs-lookup"><span data-stu-id="1e82c-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="1e82c-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e82c-128">NOTES</span></span>

## <span data-ttu-id="1e82c-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e82c-129">RELATED LINKS</span></span>
