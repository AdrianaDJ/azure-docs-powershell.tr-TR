---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
ms.openlocfilehash: 96e7be91319713ca17f6ad443596316513d2bfbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588304"
---
# <span data-ttu-id="183d5-101">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="183d5-101">Set-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="183d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="183d5-102">SYNOPSIS</span></span>
<span data-ttu-id="183d5-103">Otomasyon değişkenini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="183d5-103">Modifies an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="183d5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="183d5-104">SYNTAX</span></span>

### <span data-ttu-id="183d5-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="183d5-105">UpdateVariableValue</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="183d5-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="183d5-106">UpdateVariableDescription</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="183d5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="183d5-107">DESCRIPTION</span></span>
<span data-ttu-id="183d5-108">**Set-AzureRmAutomationVariable** cmdlet 'ı, Azure Otomasyonu 'nda bir değişkenin değerini veya açıklamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="183d5-108">The **Set-AzureRmAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="183d5-109">Değişkeni şifrelemek için, *şifrelenen* parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="183d5-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="183d5-110">Oluşturulduktan sonra bir değişkenin şifreli durumunu değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="183d5-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="183d5-111">Varolan, şifrelenmemiş, değişken için *şifrelenmiş* belirtme.</span><span class="sxs-lookup"><span data-stu-id="183d5-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="183d5-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="183d5-112">EXAMPLES</span></span>

### <span data-ttu-id="183d5-113">Örnek 1: değişkenin değerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="183d5-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="183d5-114">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki StringVariable22 adındaki değişken için yeni bir değer ayarlar.</span><span class="sxs-lookup"><span data-stu-id="183d5-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="183d5-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="183d5-115">PARAMETERS</span></span>

### <span data-ttu-id="183d5-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="183d5-116">-AutomationAccountName</span></span>
<span data-ttu-id="183d5-117">Değişkenin depolandığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="183d5-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="183d5-118">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="183d5-118">-Description</span></span>
<span data-ttu-id="183d5-119">Değişken için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="183d5-119">Specifies a description for the variable.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVariableDescription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="183d5-120">-Şifreli</span><span class="sxs-lookup"><span data-stu-id="183d5-120">-Encrypted</span></span>
<span data-ttu-id="183d5-121">Cmdlet 'in değişken değerini depolama için şifreleyip şifrelenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="183d5-121">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="183d5-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="183d5-122">-Name</span></span>
<span data-ttu-id="183d5-123">Bu cmdlet 'in değiştirdiği değişkenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="183d5-123">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="183d5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="183d5-124">-ResourceGroupName</span></span>
<span data-ttu-id="183d5-125">Bu cmdlet 'in bir değişkeni değiştirdiği kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="183d5-125">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="183d5-126">-Değer</span><span class="sxs-lookup"><span data-stu-id="183d5-126">-Value</span></span>
<span data-ttu-id="183d5-127">Değişken için bir değer belirtir.</span><span class="sxs-lookup"><span data-stu-id="183d5-127">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="183d5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="183d5-128">-DefaultProfile</span></span>
<span data-ttu-id="183d5-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="183d5-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="183d5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="183d5-130">CommonParameters</span></span>
<span data-ttu-id="183d5-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="183d5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="183d5-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="183d5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="183d5-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="183d5-133">INPUTS</span></span>

## <span data-ttu-id="183d5-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="183d5-134">OUTPUTS</span></span>

### <span data-ttu-id="183d5-135">Microsoft. Azure. Commands. Automation. model. Variable</span><span class="sxs-lookup"><span data-stu-id="183d5-135">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="183d5-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="183d5-136">NOTES</span></span>

## <span data-ttu-id="183d5-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="183d5-137">RELATED LINKS</span></span>

[<span data-ttu-id="183d5-138">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="183d5-138">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="183d5-139">Yeni-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="183d5-139">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="183d5-140">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="183d5-140">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)


