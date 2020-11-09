---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
ms.openlocfilehash: d3f76fe1e1c482c8d2913266e9c40dc5b41c62f5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321826"
---
# <span data-ttu-id="91757-101">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="91757-101">Remove-AzAutomationAccount</span></span>

## <span data-ttu-id="91757-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91757-102">SYNOPSIS</span></span>
<span data-ttu-id="91757-103">Otomasyon hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="91757-103">Removes an Automation account.</span></span>

## <span data-ttu-id="91757-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91757-104">SYNTAX</span></span>

```
Remove-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91757-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="91757-105">DESCRIPTION</span></span>
<span data-ttu-id="91757-106">**Remove-AzAutomationAccount** cmdlet 'i, bir kaynak grubundan Azure Otomasyonu hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="91757-106">The **Remove-AzAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="91757-107">Otomasyon hesapları hakkında daha fazla bilgi için New-AzAutomationAccount cmdlet bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="91757-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="91757-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91757-108">EXAMPLES</span></span>

### <span data-ttu-id="91757-109">Örnek 1: Otomasyon hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="91757-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="91757-110">Bu komut, kullanıcı doğrulaması istemeden ContosoAutomationAccount adlı bir Otomasyon hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="91757-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="91757-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91757-111">PARAMETERS</span></span>

### <span data-ttu-id="91757-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91757-112">-DefaultProfile</span></span>
<span data-ttu-id="91757-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="91757-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91757-114">-Force</span><span class="sxs-lookup"><span data-stu-id="91757-114">-Force</span></span>
<span data-ttu-id="91757-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="91757-115">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91757-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="91757-116">-Name</span></span>
<span data-ttu-id="91757-117">Bu cmdlet 'in kaldırdığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91757-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91757-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91757-118">-ResourceGroupName</span></span>
<span data-ttu-id="91757-119">Bu cmdlet 'in Otomasyon hesabını kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91757-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="91757-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="91757-120">-Confirm</span></span>
<span data-ttu-id="91757-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="91757-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91757-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91757-122">-WhatIf</span></span>
<span data-ttu-id="91757-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="91757-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91757-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="91757-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91757-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91757-125">CommonParameters</span></span>
<span data-ttu-id="91757-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91757-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91757-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91757-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91757-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91757-128">INPUTS</span></span>

### <span data-ttu-id="91757-129">System. String</span><span class="sxs-lookup"><span data-stu-id="91757-129">System.String</span></span>

## <span data-ttu-id="91757-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91757-130">OUTPUTS</span></span>

### <span data-ttu-id="91757-131">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="91757-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="91757-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91757-132">NOTES</span></span>

## <span data-ttu-id="91757-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91757-133">RELATED LINKS</span></span>

[<span data-ttu-id="91757-134">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="91757-134">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="91757-135">Yeni-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="91757-135">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="91757-136">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="91757-136">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


