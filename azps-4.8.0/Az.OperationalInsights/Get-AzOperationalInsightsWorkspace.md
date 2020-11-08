---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 1a0d36c2e871bd0495216bce18d84dff60e1044d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108804"
---
# <span data-ttu-id="2c978-101">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="2c978-101">Get-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="2c978-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c978-102">SYNOPSIS</span></span>
<span data-ttu-id="2c978-103">Çalışma alanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="2c978-103">Gets information about a workspace.</span></span>

## <span data-ttu-id="2c978-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2c978-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c978-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c978-105">DESCRIPTION</span></span>
<span data-ttu-id="2c978-106">**Get-Azoperationalınsightsworkspace** cmdlet 'i var olan bir çalışma alanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="2c978-106">The **Get-AzOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="2c978-107">Bir çalışma alanı adı belirtirseniz, bu cmdlet bu çalışma alanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="2c978-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="2c978-108">Bir ad belirtmezseniz, bu cmdlet kaynak grubundaki tüm çalışma alanları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="2c978-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="2c978-109">Bir ad ve kaynak grubu belirtmezseniz, bu cmdlet abonelikteki tüm çalışma alanları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="2c978-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="2c978-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2c978-110">EXAMPLES</span></span>

### <span data-ttu-id="2c978-111">Örnek 1: ada göre çalışma alanı alma</span><span class="sxs-lookup"><span data-stu-id="2c978-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="2c978-112">Bu komut, ContosoResourceGroup adlı kaynak grubunda MyWorkspace adlı bir çalışma alanını alır.</span><span class="sxs-lookup"><span data-stu-id="2c978-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="2c978-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2c978-113">PARAMETERS</span></span>

### <span data-ttu-id="2c978-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c978-114">-DefaultProfile</span></span>
<span data-ttu-id="2c978-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2c978-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c978-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="2c978-116">-Name</span></span>
<span data-ttu-id="2c978-117">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c978-117">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="2c978-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c978-118">-ResourceGroupName</span></span>
<span data-ttu-id="2c978-119">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c978-119">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="2c978-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c978-120">CommonParameters</span></span>
<span data-ttu-id="2c978-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2c978-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c978-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c978-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c978-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2c978-123">INPUTS</span></span>

### <span data-ttu-id="2c978-124">System. String</span><span class="sxs-lookup"><span data-stu-id="2c978-124">System.String</span></span>

## <span data-ttu-id="2c978-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2c978-125">OUTPUTS</span></span>

### <span data-ttu-id="2c978-126">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2c978-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="2c978-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2c978-127">NOTES</span></span>

## <span data-ttu-id="2c978-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2c978-128">RELATED LINKS</span></span>

[<span data-ttu-id="2c978-129">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="2c978-129">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


