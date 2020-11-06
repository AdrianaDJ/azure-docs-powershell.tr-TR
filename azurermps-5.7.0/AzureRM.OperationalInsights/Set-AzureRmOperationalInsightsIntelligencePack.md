---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
ms.openlocfilehash: c7a4a34e3969f209bcd6fcaae46ed93cd316aba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588133"
---
# <span data-ttu-id="41637-101">Set-AzureRmOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="41637-101">Set-AzureRmOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="41637-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41637-102">SYNOPSIS</span></span>
<span data-ttu-id="41637-103">Belirtilen yönetim bilgileri paketini etkinleştirilir veya devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="41637-103">Enables or disables the specified Intelligence Pack.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41637-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="41637-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41637-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="41637-105">DESCRIPTION</span></span>
<span data-ttu-id="41637-106">**Set-AzureRmOperationalInsightsIntelligencePack** cmdlet 'ı $true *etkinleştirilmişse* , belirtilen yönetim bilgileri paketi etkinleştirilir ve $false *etkinleştirilirse* bu özelliği devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="41637-106">The **Set-AzureRmOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="41637-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="41637-107">EXAMPLES</span></span>

### <span data-ttu-id="41637-108">Örnek 1: yönetim bilgileri paketlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="41637-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzureOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="41637-109">Bu komut belirtilen zekası paketini etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="41637-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="41637-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="41637-110">PARAMETERS</span></span>

### <span data-ttu-id="41637-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41637-111">-DefaultProfile</span></span>
<span data-ttu-id="41637-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="41637-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41637-113">Özellikli</span><span class="sxs-lookup"><span data-stu-id="41637-113">-Enabled</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41637-114">-Intelligencepackname</span><span class="sxs-lookup"><span data-stu-id="41637-114">-IntelligencePackName</span></span>
<span data-ttu-id="41637-115">Yönetim bilgileri paketi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="41637-115">Specifies the Intelligence Pack name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41637-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41637-116">-ResourceGroupName</span></span>
<span data-ttu-id="41637-117">Kaynak grubu adını belirtir</span><span class="sxs-lookup"><span data-stu-id="41637-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="41637-118">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="41637-118">-WorkspaceName</span></span>
<span data-ttu-id="41637-119">Çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="41637-119">Specifies the name of the workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41637-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41637-120">CommonParameters</span></span>
<span data-ttu-id="41637-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="41637-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41637-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41637-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41637-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="41637-123">INPUTS</span></span>

### <span data-ttu-id="41637-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="41637-124">None</span></span>
<span data-ttu-id="41637-125">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="41637-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="41637-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="41637-126">OUTPUTS</span></span>

## <span data-ttu-id="41637-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="41637-127">NOTES</span></span>

## <span data-ttu-id="41637-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="41637-128">RELATED LINKS</span></span>

[<span data-ttu-id="41637-129">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="41637-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


