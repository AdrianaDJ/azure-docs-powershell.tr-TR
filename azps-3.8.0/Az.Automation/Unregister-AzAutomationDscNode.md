---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
ms.openlocfilehash: d6d233bcd9ac439d163c0b6de6866a0c7dac0b04
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937884"
---
# <span data-ttu-id="0670a-101">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0670a-101">Unregister-AzAutomationDscNode</span></span>

## <span data-ttu-id="0670a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0670a-102">SYNOPSIS</span></span>
<span data-ttu-id="0670a-103">DSC düğümünü bir Otomasyon hesabıyla yönetimden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0670a-103">Removes a DSC node from management by an Automation account.</span></span>

## <span data-ttu-id="0670a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0670a-104">SYNTAX</span></span>

```
Unregister-AzAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0670a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0670a-105">DESCRIPTION</span></span>
<span data-ttu-id="0670a-106">**Unregister-AzAutomationDscNode** cmdlet 'ı bir APS Istenen durum yapılandırma (DSC) düğümünü, bir Azure Otomasyonu hesabıyla yönetimden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0670a-106">The **Unregister-AzAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="0670a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0670a-107">EXAMPLES</span></span>

### <span data-ttu-id="0670a-108">Örnek 1: Azure DSC düğümünü bir Otomasyon hesabı tarafından yönetimden kaldırma</span><span class="sxs-lookup"><span data-stu-id="0670a-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="0670a-109">Bu komut, belirtilen GUID 'ye sahip DSC düğümünü Contoso17 adlı Otomasyon hesabıyla kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0670a-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="0670a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0670a-110">PARAMETERS</span></span>

### <span data-ttu-id="0670a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0670a-111">-AutomationAccountName</span></span>
<span data-ttu-id="0670a-112">Bu cmdlet 'in DSC düğümünü kaldırdığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0670a-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="0670a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0670a-113">-DefaultProfile</span></span>
<span data-ttu-id="0670a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0670a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0670a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0670a-115">-Force</span></span>
<span data-ttu-id="0670a-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="0670a-116">ps_force</span></span>

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

### <span data-ttu-id="0670a-117">-ID</span><span class="sxs-lookup"><span data-stu-id="0670a-117">-Id</span></span>
<span data-ttu-id="0670a-118">Bu cmdlet 'in kaldırdığı DSC düğümünün benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0670a-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0670a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0670a-119">-ResourceGroupName</span></span>
<span data-ttu-id="0670a-120">Bu cmdlet 'in bir DSC düğümünü silme</span><span class="sxs-lookup"><span data-stu-id="0670a-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="0670a-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="0670a-121">-Confirm</span></span>
<span data-ttu-id="0670a-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0670a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0670a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0670a-123">-WhatIf</span></span>
<span data-ttu-id="0670a-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0670a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0670a-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0670a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0670a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0670a-126">CommonParameters</span></span>
<span data-ttu-id="0670a-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0670a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0670a-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0670a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0670a-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0670a-129">INPUTS</span></span>

### <span data-ttu-id="0670a-130">System. Guid</span><span class="sxs-lookup"><span data-stu-id="0670a-130">System.Guid</span></span>

### <span data-ttu-id="0670a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0670a-131">System.String</span></span>

## <span data-ttu-id="0670a-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0670a-132">OUTPUTS</span></span>

### <span data-ttu-id="0670a-133">Microsoft. Azure. Commands. Automation. model. DscNode</span><span class="sxs-lookup"><span data-stu-id="0670a-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="0670a-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0670a-134">NOTES</span></span>

## <span data-ttu-id="0670a-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0670a-135">RELATED LINKS</span></span>

[<span data-ttu-id="0670a-136">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0670a-136">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="0670a-137">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0670a-137">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="0670a-138">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0670a-138">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

