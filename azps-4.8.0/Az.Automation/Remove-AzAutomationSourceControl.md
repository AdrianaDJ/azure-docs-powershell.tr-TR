---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: e5422cc9254b8393330152bcaab880013b5ef99c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268114"
---
# <span data-ttu-id="ee8cc-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="ee8cc-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="ee8cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee8cc-102">SYNOPSIS</span></span>
<span data-ttu-id="ee8cc-103">Azure Otomasyonu kaynak denetimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="ee8cc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee8cc-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ee8cc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee8cc-105">DESCRIPTION</span></span>
<span data-ttu-id="ee8cc-106">Remove-AzAutomationSourceControl cmdlet 'i Azure Otomasyonu 'ndan kaynak denetimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="ee8cc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee8cc-107">EXAMPLES</span></span>

### <span data-ttu-id="ee8cc-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ee8cc-108">Example 1</span></span>
<span data-ttu-id="ee8cc-109">Bu komut, devAccount adlı hesapta VSTSNative adlı Otomasyon kaynak denetimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="ee8cc-110">Bu komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="ee8cc-111">Bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="ee8cc-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee8cc-112">PARAMETERS</span></span>

### <span data-ttu-id="ee8cc-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ee8cc-113">-AutomationAccountName</span></span>
<span data-ttu-id="ee8cc-114">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-114">The automation account name.</span></span>

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

### <span data-ttu-id="ee8cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee8cc-115">-DefaultProfile</span></span>
<span data-ttu-id="ee8cc-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee8cc-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="ee8cc-117">-Name</span></span>
<span data-ttu-id="ee8cc-118">Kaynak denetimi adı.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-118">The source control name.</span></span>

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

### <span data-ttu-id="ee8cc-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ee8cc-119">-PassThru</span></span>
<span data-ttu-id="ee8cc-120">Geçiş, çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ee8cc-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ee8cc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee8cc-122">-ResourceGroupName</span></span>
<span data-ttu-id="ee8cc-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-123">The resource group name.</span></span>

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

### <span data-ttu-id="ee8cc-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="ee8cc-124">-Confirm</span></span>
<span data-ttu-id="ee8cc-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee8cc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee8cc-126">-WhatIf</span></span>
<span data-ttu-id="ee8cc-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee8cc-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee8cc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee8cc-129">CommonParameters</span></span>
<span data-ttu-id="ee8cc-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee8cc-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee8cc-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee8cc-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee8cc-132">INPUTS</span></span>

### <span data-ttu-id="ee8cc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ee8cc-133">System.String</span></span>

## <span data-ttu-id="ee8cc-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee8cc-134">OUTPUTS</span></span>

### <span data-ttu-id="ee8cc-135">System. void</span><span class="sxs-lookup"><span data-stu-id="ee8cc-135">System.Void</span></span>

### <span data-ttu-id="ee8cc-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ee8cc-136">System.Boolean</span></span>

## <span data-ttu-id="ee8cc-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee8cc-137">NOTES</span></span>

## <span data-ttu-id="ee8cc-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee8cc-138">RELATED LINKS</span></span>
