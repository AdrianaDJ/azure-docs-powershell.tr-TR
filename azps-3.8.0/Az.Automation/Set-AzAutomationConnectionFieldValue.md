---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
ms.openlocfilehash: 2df58153b2617a8ad62b0e46544128fa47a462b5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937401"
---
# <span data-ttu-id="2d3cc-101">Set-AzAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="2d3cc-101">Set-AzAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="2d3cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d3cc-102">SYNOPSIS</span></span>
<span data-ttu-id="2d3cc-103">Otomasyon bağlantısındaki bir alanın değerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-103">Modifies the value of a field in an Automation connection.</span></span>

## <span data-ttu-id="2d3cc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d3cc-104">SYNTAX</span></span>

```
Set-AzAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d3cc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d3cc-105">DESCRIPTION</span></span>
<span data-ttu-id="2d3cc-106">**Set-AzAutomationConnectionFieldValue** cmdlet 'ı, Azure Otomasyonu 'ndaki bir bağlantı içindeki bir alanın değerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-106">The **Set-AzAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="2d3cc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d3cc-107">EXAMPLES</span></span>

### <span data-ttu-id="2d3cc-108">Örnek 1: bağlantıda alan değeri değiştirme</span><span class="sxs-lookup"><span data-stu-id="2d3cc-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="2d3cc-109">Bu komut, AutomationAccount01 adlı Otomasyon hesabındaki ContosoConnection adlı Azure bağlantısının abonelik KIMLIĞINI değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="2d3cc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d3cc-110">PARAMETERS</span></span>

### <span data-ttu-id="2d3cc-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2d3cc-111">-AutomationAccountName</span></span>
<span data-ttu-id="2d3cc-112">Bu cmdlet 'in bir bağlantı içinde bir alanı değiştirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="2d3cc-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="2d3cc-113">-ConnectionFieldName</span></span>
<span data-ttu-id="2d3cc-114">Bu cmdlet 'in değiştirdiği alanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-114">Specifies a name for the field that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d3cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d3cc-115">-DefaultProfile</span></span>
<span data-ttu-id="2d3cc-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2d3cc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d3cc-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="2d3cc-117">-Name</span></span>
<span data-ttu-id="2d3cc-118">Bu cmdlet 'in bir alanı değiştirdiği bağlantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

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

### <span data-ttu-id="2d3cc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d3cc-119">-ResourceGroupName</span></span>
<span data-ttu-id="2d3cc-120">Bu cmdlet 'in bir bağlantı içinde bir alanı değiştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="2d3cc-121">-Değer</span><span class="sxs-lookup"><span data-stu-id="2d3cc-121">-Value</span></span>
<span data-ttu-id="2d3cc-122">Bağlantı alanında değiştirilecek değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-122">Specifies a value to modify in the connection field.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d3cc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d3cc-123">CommonParameters</span></span>
<span data-ttu-id="2d3cc-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d3cc-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d3cc-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d3cc-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d3cc-126">INPUTS</span></span>

### <span data-ttu-id="2d3cc-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2d3cc-127">System.String</span></span>

### <span data-ttu-id="2d3cc-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="2d3cc-128">System.Object</span></span>

## <span data-ttu-id="2d3cc-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d3cc-129">OUTPUTS</span></span>

### <span data-ttu-id="2d3cc-130">Microsoft. Azure. Commands. Automation. model. Connection</span><span class="sxs-lookup"><span data-stu-id="2d3cc-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="2d3cc-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d3cc-131">NOTES</span></span>

## <span data-ttu-id="2d3cc-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d3cc-132">RELATED LINKS</span></span>

[<span data-ttu-id="2d3cc-133">Yeni-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="2d3cc-133">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


