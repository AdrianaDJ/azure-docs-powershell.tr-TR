---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
ms.openlocfilehash: f60e254e9addf2e7052b010033d9c81ccc6a0a98
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321853"
---
# <span data-ttu-id="30cd8-101">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="30cd8-101">New-AzAutomationVariable</span></span>

## <span data-ttu-id="30cd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="30cd8-103">Otomasyon değişkeni oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30cd8-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="30cd8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="30cd8-104">SYNTAX</span></span>

```
New-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30cd8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="30cd8-105">DESCRIPTION</span></span>
<span data-ttu-id="30cd8-106">**New-AzAutomationVariable** cmdlet 'ı Azure Otomasyonu 'nda bir değişken oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30cd8-106">The **New-AzAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="30cd8-107">Değişkeni şifrelemek için, *şifrelenen* parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="30cd8-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="30cd8-108">Oluşturulduktan sonra bir değişkenin şifreli durumunu değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="30cd8-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="30cd8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="30cd8-109">EXAMPLES</span></span>

### <span data-ttu-id="30cd8-110">Örnek 1: basit bir değer içeren bir değişken oluşturma</span><span class="sxs-lookup"><span data-stu-id="30cd8-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="30cd8-111">Bu komut, Contoso17 adlı Otomasyon hesabında dize değeriyle birlikte StringVariable22 adlı bir değişken oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30cd8-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="30cd8-112">Örnek 2: karmaşık bir değer içeren bir değişken oluşturma</span><span class="sxs-lookup"><span data-stu-id="30cd8-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="30cd8-113">İlk komut, Get-AzVM cmdlet 'ini kullanarak sanal makine alır.</span><span class="sxs-lookup"><span data-stu-id="30cd8-113">The first command gets a virtual machine by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="30cd8-114">Komut, $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="30cd8-114">The command stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="30cd8-115">İkinci komut, Contoso17 adlı Otomasyon hesabında ComplexVariable01 adlı bir değişken oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30cd8-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="30cd8-116">Bu komut, değeri için, bu örnekte $VirtualMachine sanal makinesi olan karmaşık bir nesneyi kullanır.</span><span class="sxs-lookup"><span data-stu-id="30cd8-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="30cd8-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="30cd8-117">PARAMETERS</span></span>

### <span data-ttu-id="30cd8-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="30cd8-118">-AutomationAccountName</span></span>
<span data-ttu-id="30cd8-119">Değişkenin depolanacağı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="30cd8-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="30cd8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30cd8-120">-DefaultProfile</span></span>
<span data-ttu-id="30cd8-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="30cd8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30cd8-122">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="30cd8-122">-Description</span></span>
<span data-ttu-id="30cd8-123">Değişken için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="30cd8-123">Specifies a description for the variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30cd8-124">-Şifreli</span><span class="sxs-lookup"><span data-stu-id="30cd8-124">-Encrypted</span></span>
<span data-ttu-id="30cd8-125">Bu cmdlet 'in değişkenin değerini depolama için şifreleyip şifrelenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="30cd8-125">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30cd8-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="30cd8-126">-Name</span></span>
<span data-ttu-id="30cd8-127">Değişken için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="30cd8-127">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="30cd8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30cd8-128">-ResourceGroupName</span></span>
<span data-ttu-id="30cd8-129">Bu cmdlet 'in değişken oluşturduğu kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="30cd8-129">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="30cd8-130">-Değer</span><span class="sxs-lookup"><span data-stu-id="30cd8-130">-Value</span></span>
<span data-ttu-id="30cd8-131">Değişken için bir değer belirtir.</span><span class="sxs-lookup"><span data-stu-id="30cd8-131">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30cd8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30cd8-132">CommonParameters</span></span>
<span data-ttu-id="30cd8-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="30cd8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30cd8-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30cd8-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30cd8-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="30cd8-135">INPUTS</span></span>

### <span data-ttu-id="30cd8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="30cd8-136">System.String</span></span>

### <span data-ttu-id="30cd8-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="30cd8-137">System.Boolean</span></span>

### <span data-ttu-id="30cd8-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="30cd8-138">System.Object</span></span>

## <span data-ttu-id="30cd8-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="30cd8-139">OUTPUTS</span></span>

### <span data-ttu-id="30cd8-140">Microsoft. Azure. Commands. Automation. model. Variable</span><span class="sxs-lookup"><span data-stu-id="30cd8-140">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="30cd8-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="30cd8-141">NOTES</span></span>

## <span data-ttu-id="30cd8-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="30cd8-142">RELATED LINKS</span></span>

[<span data-ttu-id="30cd8-143">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="30cd8-143">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="30cd8-144">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="30cd8-144">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="30cd8-145">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="30cd8-145">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


