---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSourceControl.md
ms.openlocfilehash: abd09a195db5652d2dfdffce17096116895eab51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588613"
---
# <span data-ttu-id="bc939-101">Remove-AzureRmAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="bc939-101">Remove-AzureRmAutomationSourceControl</span></span>

## <span data-ttu-id="bc939-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc939-102">SYNOPSIS</span></span>
<span data-ttu-id="bc939-103">Azure Otomasyonu kaynak denetimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bc939-103">Removes an Azure Automation source control.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc939-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc939-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc939-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc939-105">DESCRIPTION</span></span>
<span data-ttu-id="bc939-106">Remove-AzureRmAutomationSourceControl cmdlet 'i Azure Otomasyonu 'ndan kaynak denetimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bc939-106">The Remove-AzureRmAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="bc939-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc939-107">EXAMPLES</span></span>

### <span data-ttu-id="bc939-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bc939-108">Example 1</span></span>
<span data-ttu-id="bc939-109">Bu komut, devAccount adlı hesapta VSTSNative adlı Otomasyon kaynak denetimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bc939-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="bc939-110">Bu komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc939-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="bc939-111">Bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="bc939-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzureRmAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="bc939-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc939-112">PARAMETERS</span></span>

### <span data-ttu-id="bc939-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bc939-113">-AutomationAccountName</span></span>
<span data-ttu-id="bc939-114">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="bc939-114">The automation account name.</span></span>

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

### <span data-ttu-id="bc939-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc939-115">-DefaultProfile</span></span>
<span data-ttu-id="bc939-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bc939-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc939-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="bc939-117">-Name</span></span>
<span data-ttu-id="bc939-118">Kaynak denetimi adı.</span><span class="sxs-lookup"><span data-stu-id="bc939-118">The source control name.</span></span>

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

### <span data-ttu-id="bc939-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bc939-119">-PassThru</span></span>
<span data-ttu-id="bc939-120">Geçiş, çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="bc939-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bc939-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="bc939-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bc939-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc939-122">-ResourceGroupName</span></span>
<span data-ttu-id="bc939-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="bc939-123">The resource group name.</span></span>

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

### <span data-ttu-id="bc939-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="bc939-124">-Confirm</span></span>
<span data-ttu-id="bc939-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bc939-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc939-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc939-126">-WhatIf</span></span>
<span data-ttu-id="bc939-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bc939-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc939-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bc939-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc939-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc939-129">CommonParameters</span></span>
<span data-ttu-id="bc939-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc939-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc939-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc939-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc939-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc939-132">INPUTS</span></span>

### <span data-ttu-id="bc939-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bc939-133">System.String</span></span>

## <span data-ttu-id="bc939-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc939-134">OUTPUTS</span></span>

### <span data-ttu-id="bc939-135">Microsoft. Azure. Commands. Automation. model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="bc939-135">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="bc939-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc939-136">NOTES</span></span>

## <span data-ttu-id="bc939-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc939-137">RELATED LINKS</span></span>
