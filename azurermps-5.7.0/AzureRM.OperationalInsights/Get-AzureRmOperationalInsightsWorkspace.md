---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: b2bd8855d9c8b125b4bef72f42f0bd4a63071adb
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93595224"
---
# <span data-ttu-id="6236d-101">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="6236d-101">Get-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="6236d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6236d-102">SYNOPSIS</span></span>
<span data-ttu-id="6236d-103">Çalışma alanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="6236d-103">Gets information about a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6236d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6236d-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6236d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6236d-105">DESCRIPTION</span></span>
<span data-ttu-id="6236d-106">**Get-Azurermoperationalınsightsworkspace** cmdlet 'i var olan bir çalışma alanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="6236d-106">The **Get-AzureRmOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="6236d-107">Bir çalışma alanı adı belirtirseniz, bu cmdlet bu çalışma alanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="6236d-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="6236d-108">Bir ad belirtmezseniz, bu cmdlet kaynak grubundaki tüm çalışma alanları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="6236d-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="6236d-109">Bir ad ve kaynak grubu belirtmezseniz, bu cmdlet abonelikteki tüm çalışma alanları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="6236d-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="6236d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6236d-110">EXAMPLES</span></span>

### <span data-ttu-id="6236d-111">Örnek 1: ada göre çalışma alanı alma</span><span class="sxs-lookup"><span data-stu-id="6236d-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="6236d-112">Bu komut, ContosoResourceGroup adlı kaynak grubunda MyWorkspace adlı bir çalışma alanını alır.</span><span class="sxs-lookup"><span data-stu-id="6236d-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="6236d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6236d-113">PARAMETERS</span></span>

### <span data-ttu-id="6236d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6236d-114">-DefaultProfile</span></span>
<span data-ttu-id="6236d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6236d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6236d-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="6236d-116">-Name</span></span>
<span data-ttu-id="6236d-117">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6236d-117">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6236d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6236d-118">-ResourceGroupName</span></span>
<span data-ttu-id="6236d-119">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6236d-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6236d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6236d-120">CommonParameters</span></span>
<span data-ttu-id="6236d-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6236d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6236d-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6236d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6236d-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6236d-123">INPUTS</span></span>

### <span data-ttu-id="6236d-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6236d-124">None</span></span>
<span data-ttu-id="6236d-125">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6236d-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6236d-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6236d-126">OUTPUTS</span></span>

### <span data-ttu-id="6236d-127">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace]</span><span class="sxs-lookup"><span data-stu-id="6236d-127">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace]</span></span>

### <span data-ttu-id="6236d-128">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="6236d-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="6236d-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6236d-129">NOTES</span></span>

## <span data-ttu-id="6236d-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6236d-130">RELATED LINKS</span></span>

[<span data-ttu-id="6236d-131">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="6236d-131">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


