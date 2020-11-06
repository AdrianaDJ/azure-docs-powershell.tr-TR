---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
ms.openlocfilehash: 462566749ce0c55d4f892cc19e362f62b6fd0fa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572965"
---
# <span data-ttu-id="cd984-101">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="cd984-101">Set-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="cd984-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd984-102">SYNOPSIS</span></span>
<span data-ttu-id="cd984-103">Otomasyon değişkenini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cd984-103">Modifies an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd984-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd984-104">SYNTAX</span></span>

### <span data-ttu-id="cd984-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="cd984-105">UpdateVariableValue</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cd984-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="cd984-106">UpdateVariableDescription</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd984-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd984-107">DESCRIPTION</span></span>
<span data-ttu-id="cd984-108">**Set-AzureRmAutomationVariable** cmdlet 'ı, Azure Otomasyonu 'nda bir değişkenin değerini veya açıklamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cd984-108">The **Set-AzureRmAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="cd984-109">Değişkeni şifrelemek için, *şifrelenen* parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="cd984-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="cd984-110">Oluşturulduktan sonra bir değişkenin şifreli durumunu değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="cd984-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="cd984-111">Varolan, şifrelenmemiş, değişken için *şifrelenmiş* belirtme.</span><span class="sxs-lookup"><span data-stu-id="cd984-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="cd984-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd984-112">EXAMPLES</span></span>

### <span data-ttu-id="cd984-113">Örnek 1: değişkenin değerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="cd984-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="cd984-114">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki StringVariable22 adındaki değişken için yeni bir değer ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cd984-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="cd984-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd984-115">PARAMETERS</span></span>

### <span data-ttu-id="cd984-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cd984-116">-AutomationAccountName</span></span>
<span data-ttu-id="cd984-117">Değişkenin depolandığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd984-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="cd984-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd984-118">-DefaultProfile</span></span>
<span data-ttu-id="cd984-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="cd984-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd984-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="cd984-120">-Description</span></span>
<span data-ttu-id="cd984-121">Değişken için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd984-121">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="cd984-122">-Şifreli</span><span class="sxs-lookup"><span data-stu-id="cd984-122">-Encrypted</span></span>
<span data-ttu-id="cd984-123">Cmdlet 'in değişken değerini depolama için şifreleyip şifrelenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd984-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="cd984-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="cd984-124">-Name</span></span>
<span data-ttu-id="cd984-125">Bu cmdlet 'in değiştirdiği değişkenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd984-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cd984-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd984-126">-ResourceGroupName</span></span>
<span data-ttu-id="cd984-127">Bu cmdlet 'in bir değişkeni değiştirdiği kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd984-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="cd984-128">-Değer</span><span class="sxs-lookup"><span data-stu-id="cd984-128">-Value</span></span>
<span data-ttu-id="cd984-129">Değişken için bir değer belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd984-129">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="cd984-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd984-130">CommonParameters</span></span>
<span data-ttu-id="cd984-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd984-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd984-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd984-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd984-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd984-133">INPUTS</span></span>

### <span data-ttu-id="cd984-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cd984-134">System.String</span></span>

### <span data-ttu-id="cd984-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cd984-135">System.Boolean</span></span>

### <span data-ttu-id="cd984-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="cd984-136">System.Object</span></span>

## <span data-ttu-id="cd984-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd984-137">OUTPUTS</span></span>

### <span data-ttu-id="cd984-138">Microsoft. Azure. Commands. Automation. model. Variable</span><span class="sxs-lookup"><span data-stu-id="cd984-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="cd984-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd984-139">NOTES</span></span>

## <span data-ttu-id="cd984-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd984-140">RELATED LINKS</span></span>

[<span data-ttu-id="cd984-141">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="cd984-141">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="cd984-142">Yeni-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="cd984-142">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="cd984-143">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="cd984-143">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)


