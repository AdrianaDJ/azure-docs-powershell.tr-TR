---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
ms.openlocfilehash: fa5faafe9a7d0b7c27e5bb596e56bfadf88e5608
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763480"
---
# <span data-ttu-id="6bd85-101">Set-AzureRmAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="6bd85-101">Set-AzureRmAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="6bd85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bd85-102">SYNOPSIS</span></span>
<span data-ttu-id="6bd85-103">Otomasyon bağlantısındaki bir alanın değerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6bd85-103">Modifies the value of a field in an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bd85-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6bd85-104">SYNTAX</span></span>

```
Set-AzureRmAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6bd85-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6bd85-105">DESCRIPTION</span></span>
<span data-ttu-id="6bd85-106">**Set-AzureRmAutomationConnectionFieldValue** cmdlet 'ı, Azure Otomasyonu 'ndaki bir bağlantı içindeki alanın değerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6bd85-106">The **Set-AzureRmAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="6bd85-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6bd85-107">EXAMPLES</span></span>

### <span data-ttu-id="6bd85-108">Örnek 1: bağlantıda alan değeri değiştirme</span><span class="sxs-lookup"><span data-stu-id="6bd85-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzureRmAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="6bd85-109">Bu komut, AutomationAccount01 adlı Otomasyon hesabındaki ContosoConnection adlı Azure bağlantısının abonelik KIMLIĞINI değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6bd85-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="6bd85-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6bd85-110">PARAMETERS</span></span>

### <span data-ttu-id="6bd85-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6bd85-111">-AutomationAccountName</span></span>
<span data-ttu-id="6bd85-112">Bu cmdlet 'in bir bağlantı içinde bir alanı değiştirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bd85-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="6bd85-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="6bd85-113">-ConnectionFieldName</span></span>
<span data-ttu-id="6bd85-114">Bu cmdlet 'in değiştirdiği alanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bd85-114">Specifies a name for the field that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6bd85-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bd85-115">-DefaultProfile</span></span>
<span data-ttu-id="6bd85-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6bd85-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6bd85-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="6bd85-117">-Name</span></span>
<span data-ttu-id="6bd85-118">Bu cmdlet 'in bir alanı değiştirdiği bağlantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bd85-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

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

### <span data-ttu-id="6bd85-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bd85-119">-ResourceGroupName</span></span>
<span data-ttu-id="6bd85-120">Bu cmdlet 'in bir bağlantı içinde bir alanı değiştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bd85-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="6bd85-121">-Değer</span><span class="sxs-lookup"><span data-stu-id="6bd85-121">-Value</span></span>
<span data-ttu-id="6bd85-122">Bağlantı alanında değiştirilecek değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bd85-122">Specifies a value to modify in the connection field.</span></span>

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

### <span data-ttu-id="6bd85-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bd85-123">CommonParameters</span></span>
<span data-ttu-id="6bd85-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6bd85-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bd85-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bd85-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bd85-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6bd85-126">INPUTS</span></span>

### <span data-ttu-id="6bd85-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6bd85-127">System.String</span></span>

### <span data-ttu-id="6bd85-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="6bd85-128">System.Object</span></span>

## <span data-ttu-id="6bd85-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6bd85-129">OUTPUTS</span></span>

### <span data-ttu-id="6bd85-130">Microsoft. Azure. Commands. Automation. model. Connection</span><span class="sxs-lookup"><span data-stu-id="6bd85-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="6bd85-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6bd85-131">NOTES</span></span>

## <span data-ttu-id="6bd85-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6bd85-132">RELATED LINKS</span></span>

[<span data-ttu-id="6bd85-133">Yeni-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="6bd85-133">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)


