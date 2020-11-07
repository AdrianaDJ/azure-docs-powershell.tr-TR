---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
ms.openlocfilehash: c917089d11f4fe0ffe9ec98df5f75dec2af91f82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764729"
---
# <span data-ttu-id="96b7e-101">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="96b7e-101">Remove-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="96b7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96b7e-102">SYNOPSIS</span></span>
<span data-ttu-id="96b7e-103">Otomasyon sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="96b7e-103">Removes an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96b7e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="96b7e-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96b7e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="96b7e-105">DESCRIPTION</span></span>
<span data-ttu-id="96b7e-106">**Remove-AzureRmAutomationCertificate** cmdlet 'ı Azure Otomasyonu 'ndan sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="96b7e-106">The **Remove-AzureRmAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="96b7e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="96b7e-107">EXAMPLES</span></span>

### <span data-ttu-id="96b7e-108">Örnek 1: sertifikayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="96b7e-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="96b7e-109">Bu komut, Contoso17 adındaki Otomasyon hesabındaki Cert01 adındaki sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="96b7e-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="96b7e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="96b7e-110">PARAMETERS</span></span>

### <span data-ttu-id="96b7e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="96b7e-111">-AutomationAccountName</span></span>
<span data-ttu-id="96b7e-112">Bu cmdlet 'in sertifikayı kaldırdığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="96b7e-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="96b7e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96b7e-113">-DefaultProfile</span></span>
<span data-ttu-id="96b7e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="96b7e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96b7e-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="96b7e-115">-Name</span></span>
<span data-ttu-id="96b7e-116">Bu cmdlet 'in kaldırdığı sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="96b7e-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="96b7e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96b7e-117">-ResourceGroupName</span></span>
<span data-ttu-id="96b7e-118">Bu cmdlet 'in sertifikayı kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="96b7e-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="96b7e-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="96b7e-119">-Confirm</span></span>
<span data-ttu-id="96b7e-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="96b7e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96b7e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96b7e-121">-WhatIf</span></span>
<span data-ttu-id="96b7e-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="96b7e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96b7e-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="96b7e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96b7e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96b7e-124">CommonParameters</span></span>
<span data-ttu-id="96b7e-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="96b7e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96b7e-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96b7e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96b7e-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="96b7e-127">INPUTS</span></span>

### <span data-ttu-id="96b7e-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="96b7e-128">None</span></span>
<span data-ttu-id="96b7e-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="96b7e-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="96b7e-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="96b7e-130">OUTPUTS</span></span>

## <span data-ttu-id="96b7e-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="96b7e-131">NOTES</span></span>

## <span data-ttu-id="96b7e-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="96b7e-132">RELATED LINKS</span></span>

[<span data-ttu-id="96b7e-133">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="96b7e-133">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="96b7e-134">Yeni-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="96b7e-134">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="96b7e-135">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="96b7e-135">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


