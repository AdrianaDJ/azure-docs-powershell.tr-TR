---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacesharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
ms.openlocfilehash: 7328eda5e6821b7c403bf949460747fbf7d215e7
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93938740"
---
# <span data-ttu-id="1684a-101">Get-AzOperationalInsightsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="1684a-101">Get-AzOperationalInsightsWorkspaceSharedKey</span></span>

## <span data-ttu-id="1684a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1684a-102">SYNOPSIS</span></span>
<span data-ttu-id="1684a-103">Çalışma alanı için paylaşılan anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="1684a-103">Gets the shared keys for a workspace.</span></span>

## <span data-ttu-id="1684a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1684a-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceSharedKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1684a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1684a-105">DESCRIPTION</span></span>
<span data-ttu-id="1684a-106">**Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet 'i bir çalışma alanının paylaşılan anahtarlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="1684a-106">The **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="1684a-107">Bu tuşlar, Işlemsel Öngörüler aracılarını çalışma alanına bağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1684a-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="1684a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1684a-108">EXAMPLES</span></span>

### <span data-ttu-id="1684a-109">Örnek 1: paylaşılan anahtarları çalışma alanı adına göre alma</span><span class="sxs-lookup"><span data-stu-id="1684a-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="1684a-110">Bu komut, ContosoResourceGroup adlı kaynak grubunda MyWorkspace adlı çalışma alanı için paylaşılan anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="1684a-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="1684a-111">Örnek 2: ardışık düzeni kullanarak paylaşılan anahtarları alma</span><span class="sxs-lookup"><span data-stu-id="1684a-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceSharedKey
```

<span data-ttu-id="1684a-112">Bu komut, MyWorkspace adındaki çalışma alanını Get-AzOperationalInsightsWorkspace cmdlet 'ini kullanarak alır ve çalışma alanını **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="1684a-112">This command gets the workspace named MyWorkspace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet.</span></span>
<span data-ttu-id="1684a-113">Komut, bu çalışma alanı için paylaşılan anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="1684a-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="1684a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1684a-114">PARAMETERS</span></span>

### <span data-ttu-id="1684a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1684a-115">-DefaultProfile</span></span>
<span data-ttu-id="1684a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1684a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1684a-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="1684a-117">-Name</span></span>
<span data-ttu-id="1684a-118">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1684a-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="1684a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1684a-119">-ResourceGroupName</span></span>
<span data-ttu-id="1684a-120">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1684a-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="1684a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1684a-121">CommonParameters</span></span>
<span data-ttu-id="1684a-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1684a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1684a-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1684a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1684a-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1684a-124">INPUTS</span></span>

### <span data-ttu-id="1684a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1684a-125">System.String</span></span>

## <span data-ttu-id="1684a-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1684a-126">OUTPUTS</span></span>

### <span data-ttu-id="1684a-127">Microsoft. Azure. Commands. Operationalınsights. modeller. PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="1684a-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="1684a-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1684a-128">NOTES</span></span>

## <span data-ttu-id="1684a-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1684a-129">RELATED LINKS</span></span>

[<span data-ttu-id="1684a-130">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="1684a-130">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="1684a-131">Get-Azoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="1684a-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)

