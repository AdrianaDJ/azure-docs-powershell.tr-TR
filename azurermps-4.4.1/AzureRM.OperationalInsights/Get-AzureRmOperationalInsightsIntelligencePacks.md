---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
ms.openlocfilehash: 56bc2dd74f17daa9a56eac8ebd5128e6f074fe13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589190"
---
# <span data-ttu-id="177c0-101">Get-AzureRmOperationalInsightsIntelligencePacks</span><span class="sxs-lookup"><span data-stu-id="177c0-101">Get-AzureRmOperationalInsightsIntelligencePacks</span></span>

## <span data-ttu-id="177c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="177c0-102">SYNOPSIS</span></span>
<span data-ttu-id="177c0-103">Kullanılabilir yönetim bilgileri paketini alır.</span><span class="sxs-lookup"><span data-stu-id="177c0-103">Gets the available Intelligence Packs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="177c0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="177c0-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsIntelligencePacks [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="177c0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="177c0-105">DESCRIPTION</span></span>
<span data-ttu-id="177c0-106">**Get-AzureRmOperationalInsightsIntelligencePacks** cmdlet 'i kullanılabilir bir yönetim bilgileri paketini alır.</span><span class="sxs-lookup"><span data-stu-id="177c0-106">The **Get-AzureRmOperationalInsightsIntelligencePacks** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="177c0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="177c0-107">EXAMPLES</span></span>

### <span data-ttu-id="177c0-108">Örnek 1: yönetim bilgileri alma paketleri</span><span class="sxs-lookup"><span data-stu-id="177c0-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzureOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="177c0-109">Bu komut kullanılabilir Zektyönetim paketini alır.</span><span class="sxs-lookup"><span data-stu-id="177c0-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="177c0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="177c0-110">PARAMETERS</span></span>

### <span data-ttu-id="177c0-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="177c0-111">-ResourceGroupName</span></span>
<span data-ttu-id="177c0-112">Çalışma alanı içeren bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="177c0-112">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="177c0-113">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="177c0-113">-WorkspaceName</span></span>
<span data-ttu-id="177c0-114">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="177c0-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="177c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="177c0-115">-DefaultProfile</span></span>
<span data-ttu-id="177c0-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="177c0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="177c0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="177c0-117">CommonParameters</span></span>
<span data-ttu-id="177c0-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="177c0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="177c0-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="177c0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="177c0-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="177c0-120">INPUTS</span></span>

## <span data-ttu-id="177c0-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="177c0-121">OUTPUTS</span></span>

### <span data-ttu-id="177c0-122">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Operationalınsights. model. PSIntelligencePack]</span><span class="sxs-lookup"><span data-stu-id="177c0-122">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack]</span></span>

## <span data-ttu-id="177c0-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="177c0-123">NOTES</span></span>

## <span data-ttu-id="177c0-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="177c0-124">RELATED LINKS</span></span>

[<span data-ttu-id="177c0-125">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="177c0-125">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


