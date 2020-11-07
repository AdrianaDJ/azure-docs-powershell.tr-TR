---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsintelligencepacks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
ms.openlocfilehash: d5877e29db7c678122af93d3e5d2d6281183e410
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762306"
---
# <span data-ttu-id="d83e1-101">Get-AzureRmOperationalInsightsIntelligencePacks</span><span class="sxs-lookup"><span data-stu-id="d83e1-101">Get-AzureRmOperationalInsightsIntelligencePacks</span></span>

## <span data-ttu-id="d83e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d83e1-102">SYNOPSIS</span></span>
<span data-ttu-id="d83e1-103">Kullanılabilir yönetim bilgileri paketini alır.</span><span class="sxs-lookup"><span data-stu-id="d83e1-103">Gets the available Intelligence Packs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d83e1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d83e1-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsIntelligencePacks [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d83e1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d83e1-105">DESCRIPTION</span></span>
<span data-ttu-id="d83e1-106">**Get-AzureRmOperationalInsightsIntelligencePacks** cmdlet 'i kullanılabilir bir yönetim bilgileri paketini alır.</span><span class="sxs-lookup"><span data-stu-id="d83e1-106">The **Get-AzureRmOperationalInsightsIntelligencePacks** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="d83e1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d83e1-107">EXAMPLES</span></span>

### <span data-ttu-id="d83e1-108">Örnek 1: yönetim bilgileri alma paketleri</span><span class="sxs-lookup"><span data-stu-id="d83e1-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzureOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="d83e1-109">Bu komut kullanılabilir Zektyönetim paketini alır.</span><span class="sxs-lookup"><span data-stu-id="d83e1-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="d83e1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d83e1-110">PARAMETERS</span></span>

### <span data-ttu-id="d83e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d83e1-111">-DefaultProfile</span></span>
<span data-ttu-id="d83e1-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d83e1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d83e1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d83e1-113">-ResourceGroupName</span></span>
<span data-ttu-id="d83e1-114">Çalışma alanı içeren bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d83e1-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="d83e1-115">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="d83e1-115">-WorkspaceName</span></span>
<span data-ttu-id="d83e1-116">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d83e1-116">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d83e1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d83e1-117">CommonParameters</span></span>
<span data-ttu-id="d83e1-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d83e1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d83e1-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d83e1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d83e1-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d83e1-120">INPUTS</span></span>

### <span data-ttu-id="d83e1-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d83e1-121">System.String</span></span>

## <span data-ttu-id="d83e1-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d83e1-122">OUTPUTS</span></span>

### <span data-ttu-id="d83e1-123">Microsoft. Azure. Commands. Operationalınsights. modeller. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="d83e1-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="d83e1-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d83e1-124">NOTES</span></span>

## <span data-ttu-id="d83e1-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d83e1-125">RELATED LINKS</span></span>

[<span data-ttu-id="d83e1-126">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="d83e1-126">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


