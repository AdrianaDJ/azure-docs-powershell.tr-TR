---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
ms.openlocfilehash: 884d2a4168a4ce9efd27a6ae46387dae048f9ce1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590702"
---
# <span data-ttu-id="09d8c-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span><span class="sxs-lookup"><span data-stu-id="09d8c-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span></span>

## <span data-ttu-id="09d8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09d8c-102">SYNOPSIS</span></span>
<span data-ttu-id="09d8c-103">Çalışma alanı için paylaşılan anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="09d8c-103">Gets the shared keys for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09d8c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="09d8c-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceSharedKeys [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09d8c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="09d8c-105">DESCRIPTION</span></span>
<span data-ttu-id="09d8c-106">**Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet 'i bir çalışma alanının paylaşılan anahtarlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="09d8c-106">The **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="09d8c-107">Bu tuşlar, Işlemsel Öngörüler aracılarını çalışma alanına bağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="09d8c-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="09d8c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="09d8c-108">EXAMPLES</span></span>

### <span data-ttu-id="09d8c-109">Örnek 1: paylaşılan anahtarları çalışma alanı adına göre alma</span><span class="sxs-lookup"><span data-stu-id="09d8c-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceSharedKeys -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="09d8c-110">Bu komut, ContosoResourceGroup adlı kaynak grubunda MyWorkspace adlı çalışma alanı için paylaşılan anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="09d8c-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="09d8c-111">Örnek 2: ardışık düzeni kullanarak paylaşılan anahtarları alma</span><span class="sxs-lookup"><span data-stu-id="09d8c-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureRmOperationalInsightsWorkspaceSharedKeys
```

<span data-ttu-id="09d8c-112">Bu komut, MyWorkspace adındaki çalışma alanını Get-AzureRmOperationalInsightsWorkspace cmdlet 'ini kullanarak alır ve çalışma alanını **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="09d8c-112">This command gets the workspace named MyWorkspace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet.</span></span>
<span data-ttu-id="09d8c-113">Komut, bu çalışma alanı için paylaşılan anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="09d8c-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="09d8c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="09d8c-114">PARAMETERS</span></span>

### <span data-ttu-id="09d8c-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="09d8c-115">-Name</span></span>
<span data-ttu-id="09d8c-116">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09d8c-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="09d8c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09d8c-117">-ResourceGroupName</span></span>
<span data-ttu-id="09d8c-118">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09d8c-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="09d8c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09d8c-119">-DefaultProfile</span></span>
<span data-ttu-id="09d8c-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="09d8c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09d8c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09d8c-121">CommonParameters</span></span>
<span data-ttu-id="09d8c-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="09d8c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09d8c-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09d8c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09d8c-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="09d8c-124">INPUTS</span></span>

## <span data-ttu-id="09d8c-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="09d8c-125">OUTPUTS</span></span>

### <span data-ttu-id="09d8c-126">Microsoft. Azure. Commands. Operationalınsights. modeller. PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="09d8c-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="09d8c-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="09d8c-127">NOTES</span></span>

## <span data-ttu-id="09d8c-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="09d8c-128">RELATED LINKS</span></span>

[<span data-ttu-id="09d8c-129">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="09d8c-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="09d8c-130">Get-Azurermoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="09d8c-130">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


