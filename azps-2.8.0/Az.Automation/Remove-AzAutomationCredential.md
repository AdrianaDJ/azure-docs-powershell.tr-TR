---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
ms.openlocfilehash: 703be26244e61b797f3359ef508d92e38847bf8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753246"
---
# <span data-ttu-id="a70a4-101">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a70a4-101">Remove-AzAutomationCredential</span></span>

## <span data-ttu-id="a70a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a70a4-102">SYNOPSIS</span></span>
<span data-ttu-id="a70a4-103">Otomasyon kimlik bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a70a4-103">Removes an Automation credential.</span></span>

## <span data-ttu-id="a70a4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a70a4-104">SYNTAX</span></span>

```
Remove-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a70a4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a70a4-105">DESCRIPTION</span></span>
<span data-ttu-id="a70a4-106">**Remove-AzAutomationCredential** cmdlet 'ı Azure Otomasyonu 'ndan kimlik bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a70a4-106">The **Remove-AzAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="a70a4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a70a4-107">EXAMPLES</span></span>

### <span data-ttu-id="a70a4-108">Örnek 1: kimlik bilgisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="a70a4-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a70a4-109">Bu komut, Contoso17 adlı Azure Otomasyonu hesabında ContosoCredential adlı bir kimlik bilgisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a70a4-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="a70a4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a70a4-110">PARAMETERS</span></span>

### <span data-ttu-id="a70a4-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a70a4-111">-AutomationAccountName</span></span>
<span data-ttu-id="a70a4-112">Bu cmdlet 'in kimlik bilgilerini kaldırdığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a70a4-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="a70a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a70a4-113">-DefaultProfile</span></span>
<span data-ttu-id="a70a4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a70a4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a70a4-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="a70a4-115">-Name</span></span>
<span data-ttu-id="a70a4-116">Bu cmdlet 'in kaldırdığı kimlik bilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a70a4-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a70a4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a70a4-117">-ResourceGroupName</span></span>
<span data-ttu-id="a70a4-118">Bu cmdlet 'in kimlik bilgilerini kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a70a4-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="a70a4-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="a70a4-119">-Confirm</span></span>
<span data-ttu-id="a70a4-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a70a4-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a70a4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a70a4-121">-WhatIf</span></span>
<span data-ttu-id="a70a4-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a70a4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a70a4-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a70a4-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a70a4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a70a4-124">CommonParameters</span></span>
<span data-ttu-id="a70a4-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a70a4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a70a4-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a70a4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a70a4-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a70a4-127">INPUTS</span></span>

### <span data-ttu-id="a70a4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a70a4-128">System.String</span></span>

## <span data-ttu-id="a70a4-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a70a4-129">OUTPUTS</span></span>

### <span data-ttu-id="a70a4-130">System. void</span><span class="sxs-lookup"><span data-stu-id="a70a4-130">System.Void</span></span>

## <span data-ttu-id="a70a4-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a70a4-131">NOTES</span></span>

## <span data-ttu-id="a70a4-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a70a4-132">RELATED LINKS</span></span>

[<span data-ttu-id="a70a4-133">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a70a4-133">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="a70a4-134">Yeni-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a70a4-134">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="a70a4-135">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a70a4-135">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


