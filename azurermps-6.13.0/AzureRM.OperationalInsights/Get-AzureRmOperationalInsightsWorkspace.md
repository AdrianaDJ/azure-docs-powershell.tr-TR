---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: a88806ddd934c2c7ee4eb8bb6f463da24ecefde7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588431"
---
# <span data-ttu-id="25e4b-101">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="25e4b-101">Get-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="25e4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25e4b-102">SYNOPSIS</span></span>
<span data-ttu-id="25e4b-103">Çalışma alanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="25e4b-103">Gets information about a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25e4b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="25e4b-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25e4b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="25e4b-105">DESCRIPTION</span></span>
<span data-ttu-id="25e4b-106">**Get-Azurermoperationalınsightsworkspace** cmdlet 'i var olan bir çalışma alanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="25e4b-106">The **Get-AzureRmOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="25e4b-107">Bir çalışma alanı adı belirtirseniz, bu cmdlet bu çalışma alanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="25e4b-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="25e4b-108">Bir ad belirtmezseniz, bu cmdlet kaynak grubundaki tüm çalışma alanları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="25e4b-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="25e4b-109">Bir ad ve kaynak grubu belirtmezseniz, bu cmdlet abonelikteki tüm çalışma alanları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="25e4b-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="25e4b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="25e4b-110">EXAMPLES</span></span>

### <span data-ttu-id="25e4b-111">Örnek 1: ada göre çalışma alanı alma</span><span class="sxs-lookup"><span data-stu-id="25e4b-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="25e4b-112">Bu komut, ContosoResourceGroup adlı kaynak grubunda MyWorkspace adlı bir çalışma alanını alır.</span><span class="sxs-lookup"><span data-stu-id="25e4b-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="25e4b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="25e4b-113">PARAMETERS</span></span>

### <span data-ttu-id="25e4b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25e4b-114">-DefaultProfile</span></span>
<span data-ttu-id="25e4b-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="25e4b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25e4b-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="25e4b-116">-Name</span></span>
<span data-ttu-id="25e4b-117">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="25e4b-117">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25e4b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25e4b-118">-ResourceGroupName</span></span>
<span data-ttu-id="25e4b-119">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="25e4b-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25e4b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e4b-120">CommonParameters</span></span>
<span data-ttu-id="25e4b-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="25e4b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e4b-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25e4b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e4b-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="25e4b-123">INPUTS</span></span>

### <span data-ttu-id="25e4b-124">System. String</span><span class="sxs-lookup"><span data-stu-id="25e4b-124">System.String</span></span>

## <span data-ttu-id="25e4b-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="25e4b-125">OUTPUTS</span></span>

### <span data-ttu-id="25e4b-126">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="25e4b-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="25e4b-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="25e4b-127">NOTES</span></span>

## <span data-ttu-id="25e4b-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="25e4b-128">RELATED LINKS</span></span>

[<span data-ttu-id="25e4b-129">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="25e4b-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


