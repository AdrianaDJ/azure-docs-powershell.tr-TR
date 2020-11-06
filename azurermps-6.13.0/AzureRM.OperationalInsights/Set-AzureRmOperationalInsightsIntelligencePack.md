---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
ms.openlocfilehash: 0e8335476fc1cb511aaddb5294ea508832a04003
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588426"
---
# <span data-ttu-id="fbe2e-101">Set-AzureRmOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="fbe2e-101">Set-AzureRmOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="fbe2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbe2e-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe2e-103">Belirtilen yönetim bilgileri paketini etkinleştirilir veya devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="fbe2e-103">Enables or disables the specified Intelligence Pack.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbe2e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fbe2e-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fbe2e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fbe2e-105">DESCRIPTION</span></span>
<span data-ttu-id="fbe2e-106">**Set-AzureRmOperationalInsightsIntelligencePack** cmdlet 'ı $true *etkinleştirilmişse* , belirtilen yönetim bilgileri paketi etkinleştirilir ve $false *etkinleştirilirse* bu özelliği devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="fbe2e-106">The **Set-AzureRmOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="fbe2e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fbe2e-107">EXAMPLES</span></span>

### <span data-ttu-id="fbe2e-108">Örnek 1: yönetim bilgileri paketlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="fbe2e-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzureOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="fbe2e-109">Bu komut belirtilen zekası paketini etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="fbe2e-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="fbe2e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fbe2e-110">PARAMETERS</span></span>

### <span data-ttu-id="fbe2e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe2e-111">-DefaultProfile</span></span>
<span data-ttu-id="fbe2e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fbe2e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbe2e-113">Özellikli</span><span class="sxs-lookup"><span data-stu-id="fbe2e-113">-Enabled</span></span>
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

### <span data-ttu-id="fbe2e-114">-Intelligencepackname</span><span class="sxs-lookup"><span data-stu-id="fbe2e-114">-IntelligencePackName</span></span>
<span data-ttu-id="fbe2e-115">Yönetim bilgileri paketi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbe2e-115">Specifies the Intelligence Pack name.</span></span>

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

### <span data-ttu-id="fbe2e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbe2e-116">-ResourceGroupName</span></span>
<span data-ttu-id="fbe2e-117">Kaynak grubu adını belirtir</span><span class="sxs-lookup"><span data-stu-id="fbe2e-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="fbe2e-118">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="fbe2e-118">-WorkspaceName</span></span>
<span data-ttu-id="fbe2e-119">Çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbe2e-119">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="fbe2e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe2e-120">CommonParameters</span></span>
<span data-ttu-id="fbe2e-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fbe2e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe2e-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbe2e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe2e-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fbe2e-123">INPUTS</span></span>

### <span data-ttu-id="fbe2e-124">System. String</span><span class="sxs-lookup"><span data-stu-id="fbe2e-124">System.String</span></span>

### <span data-ttu-id="fbe2e-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fbe2e-125">System.Boolean</span></span>

## <span data-ttu-id="fbe2e-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fbe2e-126">OUTPUTS</span></span>

### <span data-ttu-id="fbe2e-127">Microsoft. Azure. Commands. Operationalınsights. modeller. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="fbe2e-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="fbe2e-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fbe2e-128">NOTES</span></span>

## <span data-ttu-id="fbe2e-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fbe2e-129">RELATED LINKS</span></span>

[<span data-ttu-id="fbe2e-130">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="fbe2e-130">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


