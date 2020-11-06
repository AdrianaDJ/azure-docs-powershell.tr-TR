---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
ms.openlocfilehash: 42fc322e9f593ecad6c295952d46274eb2563799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591166"
---
# <span data-ttu-id="db7cd-101">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="db7cd-101">Remove-AzureRmAutomationModule</span></span>

## <span data-ttu-id="db7cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db7cd-102">SYNOPSIS</span></span>
<span data-ttu-id="db7cd-103">Bir modülü Otomasyon 'dan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="db7cd-103">Removes a module from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db7cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="db7cd-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db7cd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="db7cd-105">DESCRIPTION</span></span>
<span data-ttu-id="db7cd-106">**Remove-AzureRmAutomationModule** cmdlet 'ı Azure Otomasyonu 'ndaki Otomasyon hesabından modülü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="db7cd-106">The **Remove-AzureRmAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="db7cd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="db7cd-107">EXAMPLES</span></span>

### <span data-ttu-id="db7cd-108">Örnek 1: modül kaldırma</span><span class="sxs-lookup"><span data-stu-id="db7cd-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="db7cd-109">Bu komut, Contoso17 adlı Otomasyon hesabından ContosoModule adlı bir modülü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="db7cd-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="db7cd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="db7cd-110">PARAMETERS</span></span>

### <span data-ttu-id="db7cd-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="db7cd-111">-AutomationAccountName</span></span>
<span data-ttu-id="db7cd-112">Bu cmdlet 'in modülü kaldırdığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db7cd-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="db7cd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="db7cd-113">-Force</span></span>
<span data-ttu-id="db7cd-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="db7cd-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db7cd-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="db7cd-115">-Name</span></span>
<span data-ttu-id="db7cd-116">Bu cmdlet 'in kaldırdığı modülün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db7cd-116">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="db7cd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db7cd-117">-ResourceGroupName</span></span>
<span data-ttu-id="db7cd-118">Bu cmdlet 'in modülü kaldırırken kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db7cd-118">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="db7cd-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="db7cd-119">-Confirm</span></span>
<span data-ttu-id="db7cd-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="db7cd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db7cd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db7cd-121">-WhatIf</span></span>
<span data-ttu-id="db7cd-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="db7cd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db7cd-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="db7cd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db7cd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db7cd-124">-DefaultProfile</span></span>
<span data-ttu-id="db7cd-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="db7cd-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db7cd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db7cd-126">CommonParameters</span></span>
<span data-ttu-id="db7cd-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="db7cd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db7cd-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db7cd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db7cd-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="db7cd-129">INPUTS</span></span>

## <span data-ttu-id="db7cd-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="db7cd-130">OUTPUTS</span></span>

## <span data-ttu-id="db7cd-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="db7cd-131">NOTES</span></span>

## <span data-ttu-id="db7cd-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="db7cd-132">RELATED LINKS</span></span>

[<span data-ttu-id="db7cd-133">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="db7cd-133">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="db7cd-134">Yeni-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="db7cd-134">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="db7cd-135">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="db7cd-135">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


