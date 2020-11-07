---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
ms.openlocfilehash: 266ee7c7dd8327a43de20faf0687e2f6a67ca6ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762204"
---
# <span data-ttu-id="f9dfd-101">Set-AzureRmOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="f9dfd-101">Set-AzureRmOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="f9dfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="f9dfd-103">Belirtilen yönetim bilgileri paketini etkinleştirilir veya devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-103">Enables or disables the specified Intelligence Pack.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9dfd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f9dfd-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9dfd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f9dfd-105">DESCRIPTION</span></span>
<span data-ttu-id="f9dfd-106">**Set-AzureRmOperationalInsightsIntelligencePack** cmdlet 'ı $true *etkinleştirilmişse* , belirtilen yönetim bilgileri paketi etkinleştirilir ve $false *etkinleştirilirse* bu özelliği devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-106">The **Set-AzureRmOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="f9dfd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f9dfd-107">EXAMPLES</span></span>

### <span data-ttu-id="f9dfd-108">Örnek 1: yönetim bilgileri paketlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="f9dfd-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzureOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="f9dfd-109">Bu komut belirtilen zekası paketini etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="f9dfd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f9dfd-110">PARAMETERS</span></span>

### <span data-ttu-id="f9dfd-111">Özellikli</span><span class="sxs-lookup"><span data-stu-id="f9dfd-111">-Enabled</span></span>
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9dfd-112">-Intelligencepackname</span><span class="sxs-lookup"><span data-stu-id="f9dfd-112">-IntelligencePackName</span></span>
<span data-ttu-id="f9dfd-113">Yönetim bilgileri paketi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-113">Specifies the Intelligence Pack name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9dfd-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9dfd-114">-ResourceGroupName</span></span>
<span data-ttu-id="f9dfd-115">Kaynak grubu adını belirtir</span><span class="sxs-lookup"><span data-stu-id="f9dfd-115">Specifies the resource group name</span></span>

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

### <span data-ttu-id="f9dfd-116">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="f9dfd-116">-WorkspaceName</span></span>
<span data-ttu-id="f9dfd-117">Çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-117">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="f9dfd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9dfd-118">-DefaultProfile</span></span>
<span data-ttu-id="f9dfd-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9dfd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9dfd-120">CommonParameters</span></span>
<span data-ttu-id="f9dfd-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9dfd-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9dfd-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9dfd-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f9dfd-123">INPUTS</span></span>

## <span data-ttu-id="f9dfd-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f9dfd-124">OUTPUTS</span></span>

## <span data-ttu-id="f9dfd-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f9dfd-125">NOTES</span></span>

## <span data-ttu-id="f9dfd-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f9dfd-126">RELATED LINKS</span></span>

[<span data-ttu-id="f9dfd-127">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="f9dfd-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


