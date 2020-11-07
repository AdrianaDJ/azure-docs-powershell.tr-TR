---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
ms.openlocfilehash: bc0fb96ace958761f4d6b12b73ac46b93d9a0143
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753203"
---
# <span data-ttu-id="f4928-101">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f4928-101">Set-AzAutomationVariable</span></span>

## <span data-ttu-id="f4928-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4928-102">SYNOPSIS</span></span>
<span data-ttu-id="f4928-103">Otomasyon değişkenini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f4928-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="f4928-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4928-104">SYNTAX</span></span>

### <span data-ttu-id="f4928-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="f4928-105">UpdateVariableValue</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4928-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="f4928-106">UpdateVariableDescription</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4928-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4928-107">DESCRIPTION</span></span>
<span data-ttu-id="f4928-108">**Set-AzAutomationVariable** cmdlet 'ı, Azure Otomasyonu 'nda bir değişkenin değerini veya açıklamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f4928-108">The **Set-AzAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="f4928-109">Değişkeni şifrelemek için, *şifrelenen* parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="f4928-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="f4928-110">Oluşturulduktan sonra bir değişkenin şifreli durumunu değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="f4928-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="f4928-111">Varolan, şifrelenmemiş, değişken için *şifrelenmiş* belirtme.</span><span class="sxs-lookup"><span data-stu-id="f4928-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="f4928-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4928-112">EXAMPLES</span></span>

### <span data-ttu-id="f4928-113">Örnek 1: değişkenin değerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="f4928-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="f4928-114">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki StringVariable22 adındaki değişken için yeni bir değer ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f4928-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="f4928-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4928-115">PARAMETERS</span></span>

### <span data-ttu-id="f4928-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f4928-116">-AutomationAccountName</span></span>
<span data-ttu-id="f4928-117">Değişkenin depolandığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4928-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="f4928-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4928-118">-DefaultProfile</span></span>
<span data-ttu-id="f4928-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f4928-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4928-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="f4928-120">-Description</span></span>
<span data-ttu-id="f4928-121">Değişken için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4928-121">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="f4928-122">-Şifreli</span><span class="sxs-lookup"><span data-stu-id="f4928-122">-Encrypted</span></span>
<span data-ttu-id="f4928-123">Cmdlet 'in değişken değerini depolama için şifreleyip şifrelenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4928-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="f4928-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="f4928-124">-Name</span></span>
<span data-ttu-id="f4928-125">Bu cmdlet 'in değiştirdiği değişkenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4928-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f4928-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4928-126">-ResourceGroupName</span></span>
<span data-ttu-id="f4928-127">Bu cmdlet 'in bir değişkeni değiştirdiği kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4928-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="f4928-128">-Değer</span><span class="sxs-lookup"><span data-stu-id="f4928-128">-Value</span></span>
<span data-ttu-id="f4928-129">Değişken için bir değer belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4928-129">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="f4928-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4928-130">CommonParameters</span></span>
<span data-ttu-id="f4928-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4928-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4928-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4928-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4928-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4928-133">INPUTS</span></span>

### <span data-ttu-id="f4928-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f4928-134">System.String</span></span>

### <span data-ttu-id="f4928-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4928-135">System.Boolean</span></span>

### <span data-ttu-id="f4928-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="f4928-136">System.Object</span></span>

## <span data-ttu-id="f4928-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4928-137">OUTPUTS</span></span>

### <span data-ttu-id="f4928-138">Microsoft. Azure. Commands. Automation. model. Variable</span><span class="sxs-lookup"><span data-stu-id="f4928-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="f4928-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4928-139">NOTES</span></span>

## <span data-ttu-id="f4928-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4928-140">RELATED LINKS</span></span>

[<span data-ttu-id="f4928-141">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f4928-141">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="f4928-142">Yeni-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f4928-142">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="f4928-143">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f4928-143">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)


