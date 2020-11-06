---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
ms.openlocfilehash: 6c0fe1185bfa8d5233371788da87e7a13fe32c6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587309"
---
# <span data-ttu-id="6710f-101">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6710f-101">Remove-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="6710f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6710f-102">SYNOPSIS</span></span>
<span data-ttu-id="6710f-103">Otomasyon kimlik bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6710f-103">Removes an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6710f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6710f-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6710f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6710f-105">DESCRIPTION</span></span>
<span data-ttu-id="6710f-106">**Remove-AzureRmAutomationCredential** cmdlet 'ı Azure Otomasyonu 'ndan kimlik bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6710f-106">The **Remove-AzureRmAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="6710f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6710f-107">EXAMPLES</span></span>

### <span data-ttu-id="6710f-108">Örnek 1: kimlik bilgisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="6710f-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6710f-109">Bu komut, Contoso17 adlı Azure Otomasyonu hesabında ContosoCredential adlı bir kimlik bilgisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6710f-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="6710f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6710f-110">PARAMETERS</span></span>

### <span data-ttu-id="6710f-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6710f-111">-AutomationAccountName</span></span>
<span data-ttu-id="6710f-112">Bu cmdlet 'in kimlik bilgilerini kaldırdığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6710f-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="6710f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6710f-113">-DefaultProfile</span></span>
<span data-ttu-id="6710f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6710f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6710f-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="6710f-115">-Name</span></span>
<span data-ttu-id="6710f-116">Bu cmdlet 'in kaldırdığı kimlik bilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6710f-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6710f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6710f-117">-ResourceGroupName</span></span>
<span data-ttu-id="6710f-118">Bu cmdlet 'in kimlik bilgilerini kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6710f-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="6710f-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="6710f-119">-Confirm</span></span>
<span data-ttu-id="6710f-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6710f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6710f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6710f-121">-WhatIf</span></span>
<span data-ttu-id="6710f-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6710f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6710f-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6710f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6710f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6710f-124">CommonParameters</span></span>
<span data-ttu-id="6710f-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6710f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6710f-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6710f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6710f-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6710f-127">INPUTS</span></span>

### <span data-ttu-id="6710f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6710f-128">System.String</span></span>

## <span data-ttu-id="6710f-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6710f-129">OUTPUTS</span></span>

### <span data-ttu-id="6710f-130">System. void</span><span class="sxs-lookup"><span data-stu-id="6710f-130">System.Void</span></span>

## <span data-ttu-id="6710f-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6710f-131">NOTES</span></span>

## <span data-ttu-id="6710f-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6710f-132">RELATED LINKS</span></span>

[<span data-ttu-id="6710f-133">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6710f-133">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="6710f-134">Yeni-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6710f-134">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="6710f-135">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6710f-135">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


