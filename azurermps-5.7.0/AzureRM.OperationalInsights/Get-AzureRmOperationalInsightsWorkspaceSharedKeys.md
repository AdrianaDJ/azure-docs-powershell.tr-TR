---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspacesharedkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
ms.openlocfilehash: 5fab6a3a0419047fef32f5bf32f52e1f7ee57d3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588145"
---
# <span data-ttu-id="fc38f-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span><span class="sxs-lookup"><span data-stu-id="fc38f-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span></span>

## <span data-ttu-id="fc38f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc38f-102">SYNOPSIS</span></span>
<span data-ttu-id="fc38f-103">Çalışma alanı için paylaşılan anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="fc38f-103">Gets the shared keys for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc38f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc38f-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceSharedKeys [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc38f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc38f-105">DESCRIPTION</span></span>
<span data-ttu-id="fc38f-106">**Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet 'i bir çalışma alanının paylaşılan anahtarlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="fc38f-106">The **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="fc38f-107">Bu tuşlar, Işlemsel Öngörüler aracılarını çalışma alanına bağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fc38f-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="fc38f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc38f-108">EXAMPLES</span></span>

### <span data-ttu-id="fc38f-109">Örnek 1: paylaşılan anahtarları çalışma alanı adına göre alma</span><span class="sxs-lookup"><span data-stu-id="fc38f-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceSharedKeys -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="fc38f-110">Bu komut, ContosoResourceGroup adlı kaynak grubunda MyWorkspace adlı çalışma alanı için paylaşılan anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="fc38f-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="fc38f-111">Örnek 2: ardışık düzeni kullanarak paylaşılan anahtarları alma</span><span class="sxs-lookup"><span data-stu-id="fc38f-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureRmOperationalInsightsWorkspaceSharedKeys
```

<span data-ttu-id="fc38f-112">Bu komut, MyWorkspace adındaki çalışma alanını Get-AzureRmOperationalInsightsWorkspace cmdlet 'ini kullanarak alır ve çalışma alanını **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="fc38f-112">This command gets the workspace named MyWorkspace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet.</span></span>
<span data-ttu-id="fc38f-113">Komut, bu çalışma alanı için paylaşılan anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="fc38f-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="fc38f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc38f-114">PARAMETERS</span></span>

### <span data-ttu-id="fc38f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc38f-115">-DefaultProfile</span></span>
<span data-ttu-id="fc38f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fc38f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc38f-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="fc38f-117">-Name</span></span>
<span data-ttu-id="fc38f-118">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc38f-118">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc38f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc38f-119">-ResourceGroupName</span></span>
<span data-ttu-id="fc38f-120">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc38f-120">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc38f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc38f-121">CommonParameters</span></span>
<span data-ttu-id="fc38f-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc38f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc38f-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc38f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc38f-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc38f-124">INPUTS</span></span>

### <span data-ttu-id="fc38f-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="fc38f-125">None</span></span>
<span data-ttu-id="fc38f-126">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="fc38f-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fc38f-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc38f-127">OUTPUTS</span></span>

### <span data-ttu-id="fc38f-128">Microsoft. Azure. Commands. Operationalınsights. modeller. PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="fc38f-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="fc38f-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc38f-129">NOTES</span></span>

## <span data-ttu-id="fc38f-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc38f-130">RELATED LINKS</span></span>

[<span data-ttu-id="fc38f-131">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="fc38f-131">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="fc38f-132">Get-Azurermoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="fc38f-132">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


