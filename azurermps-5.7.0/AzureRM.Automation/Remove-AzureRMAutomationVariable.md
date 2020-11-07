---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
ms.openlocfilehash: dea9f62583cca8f3a5ee9ce05b6b7e60e8bf4755
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590526"
---
# <span data-ttu-id="b28ed-101">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b28ed-101">Remove-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="b28ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b28ed-102">SYNOPSIS</span></span>
<span data-ttu-id="b28ed-103">Otomasyon değişkenini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b28ed-103">Removes an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b28ed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b28ed-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b28ed-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b28ed-105">DESCRIPTION</span></span>
<span data-ttu-id="b28ed-106">**Remove-AzureRmAutomationVariable** cmdlet 'ı Azure Otomasyonu 'ndan bir değişkeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b28ed-106">The **Remove-AzureRmAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="b28ed-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b28ed-107">EXAMPLES</span></span>

### <span data-ttu-id="b28ed-108">Örnek 1: bir değişkeni kaldırma</span><span class="sxs-lookup"><span data-stu-id="b28ed-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b28ed-109">Bu komut, Contoso17 adındaki Otomasyon hesabındaki StringVariable22 adlı bir değişkeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b28ed-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="b28ed-110">Bu komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b28ed-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="b28ed-111">Bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="b28ed-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b28ed-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b28ed-112">PARAMETERS</span></span>

### <span data-ttu-id="b28ed-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b28ed-113">-AutomationAccountName</span></span>
<span data-ttu-id="b28ed-114">Bu cmdlet 'in sildiği değişkeni içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b28ed-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b28ed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b28ed-115">-DefaultProfile</span></span>
<span data-ttu-id="b28ed-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b28ed-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b28ed-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="b28ed-117">-Name</span></span>
<span data-ttu-id="b28ed-118">Bu cmdlet 'in sildiği değişkenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b28ed-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="b28ed-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b28ed-119">-ResourceGroupName</span></span>
<span data-ttu-id="b28ed-120">Bu cmdlet 'in bir değişkeni sildiği kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b28ed-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="b28ed-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="b28ed-121">-Confirm</span></span>
<span data-ttu-id="b28ed-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b28ed-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b28ed-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b28ed-123">-WhatIf</span></span>
<span data-ttu-id="b28ed-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b28ed-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b28ed-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b28ed-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b28ed-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b28ed-126">CommonParameters</span></span>
<span data-ttu-id="b28ed-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b28ed-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b28ed-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b28ed-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b28ed-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b28ed-129">INPUTS</span></span>

### <span data-ttu-id="b28ed-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b28ed-130">None</span></span>
<span data-ttu-id="b28ed-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b28ed-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b28ed-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b28ed-132">OUTPUTS</span></span>

### <span data-ttu-id="b28ed-133">Microsoft. Azure. Commands. Automation. model. Variable</span><span class="sxs-lookup"><span data-stu-id="b28ed-133">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="b28ed-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b28ed-134">NOTES</span></span>

## <span data-ttu-id="b28ed-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b28ed-135">RELATED LINKS</span></span>

[<span data-ttu-id="b28ed-136">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b28ed-136">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="b28ed-137">Yeni-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b28ed-137">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="b28ed-138">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b28ed-138">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)

