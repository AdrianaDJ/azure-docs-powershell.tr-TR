---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
ms.openlocfilehash: 9932627e94a27c1b29d20a5a6bc49d47a55d3ef5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753254"
---
# <span data-ttu-id="7904c-101">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="7904c-101">Remove-AzAutomationCertificate</span></span>

## <span data-ttu-id="7904c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7904c-102">SYNOPSIS</span></span>
<span data-ttu-id="7904c-103">Otomasyon sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7904c-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="7904c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7904c-104">SYNTAX</span></span>

```
Remove-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7904c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7904c-105">DESCRIPTION</span></span>
<span data-ttu-id="7904c-106">**Remove-AzAutomationCertificate** cmdlet 'ı Azure Otomasyonu 'ndan sertifikayı çıkarır.</span><span class="sxs-lookup"><span data-stu-id="7904c-106">The **Remove-AzAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="7904c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7904c-107">EXAMPLES</span></span>

### <span data-ttu-id="7904c-108">Örnek 1: sertifikayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="7904c-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7904c-109">Bu komut, Contoso17 adındaki Otomasyon hesabındaki Cert01 adındaki sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7904c-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="7904c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7904c-110">PARAMETERS</span></span>

### <span data-ttu-id="7904c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7904c-111">-AutomationAccountName</span></span>
<span data-ttu-id="7904c-112">Bu cmdlet 'in sertifikayı kaldırdığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7904c-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="7904c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7904c-113">-DefaultProfile</span></span>
<span data-ttu-id="7904c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7904c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7904c-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="7904c-115">-Name</span></span>
<span data-ttu-id="7904c-116">Bu cmdlet 'in kaldırdığı sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7904c-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7904c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7904c-117">-ResourceGroupName</span></span>
<span data-ttu-id="7904c-118">Bu cmdlet 'in sertifikayı kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7904c-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="7904c-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="7904c-119">-Confirm</span></span>
<span data-ttu-id="7904c-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7904c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7904c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7904c-121">-WhatIf</span></span>
<span data-ttu-id="7904c-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7904c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7904c-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7904c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7904c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7904c-124">CommonParameters</span></span>
<span data-ttu-id="7904c-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7904c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7904c-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7904c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7904c-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7904c-127">INPUTS</span></span>

### <span data-ttu-id="7904c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7904c-128">System.String</span></span>

## <span data-ttu-id="7904c-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7904c-129">OUTPUTS</span></span>

### <span data-ttu-id="7904c-130">System. void</span><span class="sxs-lookup"><span data-stu-id="7904c-130">System.Void</span></span>

## <span data-ttu-id="7904c-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7904c-131">NOTES</span></span>

## <span data-ttu-id="7904c-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7904c-132">RELATED LINKS</span></span>

[<span data-ttu-id="7904c-133">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="7904c-133">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="7904c-134">Yeni-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="7904c-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="7904c-135">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="7904c-135">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


