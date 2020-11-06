---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
ms.openlocfilehash: d1230030f95d22d972aa537208b30f350ec9dbe4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591821"
---
# <span data-ttu-id="4d7f8-101">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4d7f8-101">Remove-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="4d7f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d7f8-102">SYNOPSIS</span></span>
<span data-ttu-id="4d7f8-103">Otomasyon sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4d7f8-103">Removes an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d7f8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d7f8-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d7f8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d7f8-105">DESCRIPTION</span></span>
<span data-ttu-id="4d7f8-106">**Remove-AzureRmAutomationCertificate** cmdlet 'ı Azure Otomasyonu 'ndan sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4d7f8-106">The **Remove-AzureRmAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="4d7f8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d7f8-107">EXAMPLES</span></span>

### <span data-ttu-id="4d7f8-108">Örnek 1: sertifikayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="4d7f8-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4d7f8-109">Bu komut, Contoso17 adındaki Otomasyon hesabındaki Cert01 adındaki sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4d7f8-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="4d7f8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d7f8-110">PARAMETERS</span></span>

### <span data-ttu-id="4d7f8-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4d7f8-111">-AutomationAccountName</span></span>
<span data-ttu-id="4d7f8-112">Bu cmdlet 'in sertifikayı kaldırdığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d7f8-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="4d7f8-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="4d7f8-113">-Name</span></span>
<span data-ttu-id="4d7f8-114">Bu cmdlet 'in kaldırdığı sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d7f8-114">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4d7f8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d7f8-115">-ResourceGroupName</span></span>
<span data-ttu-id="4d7f8-116">Bu cmdlet 'in sertifikayı kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d7f8-116">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="4d7f8-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="4d7f8-117">-Confirm</span></span>
<span data-ttu-id="4d7f8-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4d7f8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d7f8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d7f8-119">-WhatIf</span></span>
<span data-ttu-id="4d7f8-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d7f8-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d7f8-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4d7f8-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d7f8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d7f8-122">-DefaultProfile</span></span>
<span data-ttu-id="4d7f8-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4d7f8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d7f8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d7f8-124">CommonParameters</span></span>
<span data-ttu-id="4d7f8-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d7f8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d7f8-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d7f8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d7f8-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d7f8-127">INPUTS</span></span>

## <span data-ttu-id="4d7f8-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d7f8-128">OUTPUTS</span></span>

## <span data-ttu-id="4d7f8-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d7f8-129">NOTES</span></span>

## <span data-ttu-id="4d7f8-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d7f8-130">RELATED LINKS</span></span>

[<span data-ttu-id="4d7f8-131">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4d7f8-131">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="4d7f8-132">Yeni-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4d7f8-132">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="4d7f8-133">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4d7f8-133">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


