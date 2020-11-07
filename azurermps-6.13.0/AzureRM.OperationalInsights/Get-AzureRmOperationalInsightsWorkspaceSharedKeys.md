---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspacesharedkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
ms.openlocfilehash: 07d0834b89010ff533e1620f29904ea159d3dfea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764129"
---
# <span data-ttu-id="dbffd-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span><span class="sxs-lookup"><span data-stu-id="dbffd-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span></span>

## <span data-ttu-id="dbffd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbffd-102">SYNOPSIS</span></span>
<span data-ttu-id="dbffd-103">Çalışma alanı için paylaşılan anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="dbffd-103">Gets the shared keys for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbffd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dbffd-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceSharedKeys [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbffd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dbffd-105">DESCRIPTION</span></span>
<span data-ttu-id="dbffd-106">**Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet 'i bir çalışma alanının paylaşılan anahtarlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="dbffd-106">The **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="dbffd-107">Bu tuşlar, Işlemsel Öngörüler aracılarını çalışma alanına bağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dbffd-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="dbffd-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dbffd-108">EXAMPLES</span></span>

### <span data-ttu-id="dbffd-109">Örnek 1: paylaşılan anahtarları çalışma alanı adına göre alma</span><span class="sxs-lookup"><span data-stu-id="dbffd-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceSharedKeys -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="dbffd-110">Bu komut, ContosoResourceGroup adlı kaynak grubunda MyWorkspace adlı çalışma alanı için paylaşılan anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="dbffd-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="dbffd-111">Örnek 2: ardışık düzeni kullanarak paylaşılan anahtarları alma</span><span class="sxs-lookup"><span data-stu-id="dbffd-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureRmOperationalInsightsWorkspaceSharedKeys
```

<span data-ttu-id="dbffd-112">Bu komut, MyWorkspace adındaki çalışma alanını Get-AzureRmOperationalInsightsWorkspace cmdlet 'ini kullanarak alır ve çalışma alanını **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="dbffd-112">This command gets the workspace named MyWorkspace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet.</span></span>
<span data-ttu-id="dbffd-113">Komut, bu çalışma alanı için paylaşılan anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="dbffd-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="dbffd-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dbffd-114">PARAMETERS</span></span>

### <span data-ttu-id="dbffd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbffd-115">-DefaultProfile</span></span>
<span data-ttu-id="dbffd-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="dbffd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbffd-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="dbffd-117">-Name</span></span>
<span data-ttu-id="dbffd-118">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dbffd-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbffd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbffd-119">-ResourceGroupName</span></span>
<span data-ttu-id="dbffd-120">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dbffd-120">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbffd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbffd-121">CommonParameters</span></span>
<span data-ttu-id="dbffd-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dbffd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbffd-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbffd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbffd-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dbffd-124">INPUTS</span></span>

### <span data-ttu-id="dbffd-125">System. String</span><span class="sxs-lookup"><span data-stu-id="dbffd-125">System.String</span></span>

## <span data-ttu-id="dbffd-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dbffd-126">OUTPUTS</span></span>

### <span data-ttu-id="dbffd-127">Microsoft. Azure. Commands. Operationalınsights. modeller. PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="dbffd-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="dbffd-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dbffd-128">NOTES</span></span>

## <span data-ttu-id="dbffd-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dbffd-129">RELATED LINKS</span></span>

[<span data-ttu-id="dbffd-130">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="dbffd-130">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="dbffd-131">Get-Azurermoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="dbffd-131">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


