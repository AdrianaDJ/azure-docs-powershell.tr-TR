---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
ms.openlocfilehash: 11b6772325c3e5170c697b21d25092fd96f3e2e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764725"
---
# <span data-ttu-id="2c7a2-101">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="2c7a2-101">Remove-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="2c7a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c7a2-102">SYNOPSIS</span></span>
<span data-ttu-id="2c7a2-103">Otomasyon kimlik bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2c7a2-103">Removes an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c7a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2c7a2-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c7a2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c7a2-105">DESCRIPTION</span></span>
<span data-ttu-id="2c7a2-106">**Remove-AzureRmAutomationCredential** cmdlet 'ı Azure Otomasyonu 'ndan kimlik bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2c7a2-106">The **Remove-AzureRmAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="2c7a2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2c7a2-107">EXAMPLES</span></span>

### <span data-ttu-id="2c7a2-108">Örnek 1: kimlik bilgisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="2c7a2-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2c7a2-109">Bu komut, Contoso17 adlı Azure Otomasyonu hesabında ContosoCredential adlı bir kimlik bilgisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2c7a2-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="2c7a2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2c7a2-110">PARAMETERS</span></span>

### <span data-ttu-id="2c7a2-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2c7a2-111">-AutomationAccountName</span></span>
<span data-ttu-id="2c7a2-112">Bu cmdlet 'in kimlik bilgilerini kaldırdığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c7a2-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="2c7a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c7a2-113">-DefaultProfile</span></span>
<span data-ttu-id="2c7a2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2c7a2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c7a2-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="2c7a2-115">-Name</span></span>
<span data-ttu-id="2c7a2-116">Bu cmdlet 'in kaldırdığı kimlik bilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c7a2-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2c7a2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c7a2-117">-ResourceGroupName</span></span>
<span data-ttu-id="2c7a2-118">Bu cmdlet 'in kimlik bilgilerini kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c7a2-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="2c7a2-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="2c7a2-119">-Confirm</span></span>
<span data-ttu-id="2c7a2-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2c7a2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c7a2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c7a2-121">-WhatIf</span></span>
<span data-ttu-id="2c7a2-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2c7a2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c7a2-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2c7a2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c7a2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c7a2-124">CommonParameters</span></span>
<span data-ttu-id="2c7a2-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2c7a2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c7a2-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c7a2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c7a2-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2c7a2-127">INPUTS</span></span>

### <span data-ttu-id="2c7a2-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2c7a2-128">None</span></span>
<span data-ttu-id="2c7a2-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="2c7a2-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2c7a2-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2c7a2-130">OUTPUTS</span></span>

## <span data-ttu-id="2c7a2-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2c7a2-131">NOTES</span></span>

## <span data-ttu-id="2c7a2-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2c7a2-132">RELATED LINKS</span></span>

[<span data-ttu-id="2c7a2-133">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="2c7a2-133">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="2c7a2-134">Yeni-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="2c7a2-134">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="2c7a2-135">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="2c7a2-135">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


