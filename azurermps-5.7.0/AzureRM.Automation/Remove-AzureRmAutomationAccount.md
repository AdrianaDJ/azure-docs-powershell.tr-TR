---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
ms.openlocfilehash: 854a5bd2fb9644d6060810edba44ac7082eb6903
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590525"
---
# <span data-ttu-id="96215-101">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="96215-101">Remove-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="96215-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96215-102">SYNOPSIS</span></span>
<span data-ttu-id="96215-103">Otomasyon hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="96215-103">Removes an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96215-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="96215-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96215-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="96215-105">DESCRIPTION</span></span>
<span data-ttu-id="96215-106">**Remove-AzureRmAutomationAccount** cmdlet 'i, bir kaynak grubundan Azure Otomasyonu hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="96215-106">The **Remove-AzureRmAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>

<span data-ttu-id="96215-107">Otomasyon hesapları hakkında daha fazla bilgi için New-AzureRmAutomationAccount cmdlet bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="96215-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="96215-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="96215-108">EXAMPLES</span></span>

### <span data-ttu-id="96215-109">Örnek 1: Otomasyon hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="96215-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="96215-110">Bu komut, kullanıcı doğrulaması istemeden ContosoAutomationAccount adlı bir Otomasyon hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="96215-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="96215-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="96215-111">PARAMETERS</span></span>

### <span data-ttu-id="96215-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96215-112">-DefaultProfile</span></span>
<span data-ttu-id="96215-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="96215-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96215-114">-Force</span><span class="sxs-lookup"><span data-stu-id="96215-114">-Force</span></span>
<span data-ttu-id="96215-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="96215-115">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96215-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="96215-116">-Name</span></span>
<span data-ttu-id="96215-117">Bu cmdlet 'in kaldırdığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="96215-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96215-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96215-118">-ResourceGroupName</span></span>
<span data-ttu-id="96215-119">Bu cmdlet 'in Otomasyon hesabını kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="96215-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="96215-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="96215-120">-Confirm</span></span>
<span data-ttu-id="96215-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="96215-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96215-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96215-122">-WhatIf</span></span>
<span data-ttu-id="96215-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="96215-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96215-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="96215-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96215-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96215-125">CommonParameters</span></span>
<span data-ttu-id="96215-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="96215-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96215-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96215-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96215-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="96215-128">INPUTS</span></span>

### <span data-ttu-id="96215-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="96215-129">None</span></span>
<span data-ttu-id="96215-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="96215-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="96215-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="96215-131">OUTPUTS</span></span>

### <span data-ttu-id="96215-132">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="96215-132">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="96215-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="96215-133">NOTES</span></span>

## <span data-ttu-id="96215-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="96215-134">RELATED LINKS</span></span>

[<span data-ttu-id="96215-135">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="96215-135">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="96215-136">Yeni-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="96215-136">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="96215-137">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="96215-137">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


