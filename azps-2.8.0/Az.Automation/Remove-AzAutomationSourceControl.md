---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: 165850e0212969fea76e85f209d3fcf7c2040b79
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753235"
---
# <span data-ttu-id="3f10e-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="3f10e-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="3f10e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f10e-102">SYNOPSIS</span></span>
<span data-ttu-id="3f10e-103">Azure Otomasyonu kaynak denetimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3f10e-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="3f10e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3f10e-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f10e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3f10e-105">DESCRIPTION</span></span>
<span data-ttu-id="3f10e-106">Remove-AzAutomationSourceControl cmdlet 'i Azure Otomasyonu 'ndan kaynak denetimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3f10e-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="3f10e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3f10e-107">EXAMPLES</span></span>

### <span data-ttu-id="3f10e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3f10e-108">Example 1</span></span>
<span data-ttu-id="3f10e-109">Bu komut, devAccount adlı hesapta VSTSNative adlı Otomasyon kaynak denetimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3f10e-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="3f10e-110">Bu komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f10e-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="3f10e-111">Bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="3f10e-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="3f10e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3f10e-112">PARAMETERS</span></span>

### <span data-ttu-id="3f10e-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3f10e-113">-AutomationAccountName</span></span>
<span data-ttu-id="3f10e-114">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="3f10e-114">The automation account name.</span></span>

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

### <span data-ttu-id="3f10e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f10e-115">-DefaultProfile</span></span>
<span data-ttu-id="3f10e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3f10e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f10e-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="3f10e-117">-Name</span></span>
<span data-ttu-id="3f10e-118">Kaynak denetimi adı.</span><span class="sxs-lookup"><span data-stu-id="3f10e-118">The source control name.</span></span>

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

### <span data-ttu-id="3f10e-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3f10e-119">-PassThru</span></span>
<span data-ttu-id="3f10e-120">Geçiş, çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="3f10e-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3f10e-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="3f10e-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f10e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f10e-122">-ResourceGroupName</span></span>
<span data-ttu-id="3f10e-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3f10e-123">The resource group name.</span></span>

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

### <span data-ttu-id="3f10e-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="3f10e-124">-Confirm</span></span>
<span data-ttu-id="3f10e-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3f10e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f10e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f10e-126">-WhatIf</span></span>
<span data-ttu-id="3f10e-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f10e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f10e-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3f10e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f10e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f10e-129">CommonParameters</span></span>
<span data-ttu-id="3f10e-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3f10e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f10e-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f10e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f10e-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3f10e-132">INPUTS</span></span>

### <span data-ttu-id="3f10e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3f10e-133">System.String</span></span>

## <span data-ttu-id="3f10e-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3f10e-134">OUTPUTS</span></span>

### <span data-ttu-id="3f10e-135">System. void</span><span class="sxs-lookup"><span data-stu-id="3f10e-135">System.Void</span></span>

### <span data-ttu-id="3f10e-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3f10e-136">System.Boolean</span></span>

## <span data-ttu-id="3f10e-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3f10e-137">NOTES</span></span>

## <span data-ttu-id="3f10e-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3f10e-138">RELATED LINKS</span></span>
