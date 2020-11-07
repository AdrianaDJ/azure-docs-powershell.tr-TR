---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
ms.openlocfilehash: fc4696a26c10ace497c6ff64a7ac4c1ac49279c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761480"
---
# <span data-ttu-id="b3101-101">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b3101-101">Unregister-AzAutomationDscNode</span></span>

## <span data-ttu-id="b3101-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3101-102">SYNOPSIS</span></span>
<span data-ttu-id="b3101-103">DSC düğümünü bir Otomasyon hesabıyla yönetimden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b3101-103">Removes a DSC node from management by an Automation account.</span></span>

## <span data-ttu-id="b3101-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3101-104">SYNTAX</span></span>

```
Unregister-AzAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3101-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3101-105">DESCRIPTION</span></span>
<span data-ttu-id="b3101-106">**Unregister-AzAutomationDscNode** cmdlet 'ı bir APS Istenen durum yapılandırma (DSC) düğümünü, bir Azure Otomasyonu hesabıyla yönetimden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b3101-106">The **Unregister-AzAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="b3101-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3101-107">EXAMPLES</span></span>

### <span data-ttu-id="b3101-108">Örnek 1: Azure DSC düğümünü bir Otomasyon hesabı tarafından yönetimden kaldırma</span><span class="sxs-lookup"><span data-stu-id="b3101-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="b3101-109">Bu komut, belirtilen GUID 'ye sahip DSC düğümünü Contoso17 adlı Otomasyon hesabıyla kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b3101-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="b3101-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3101-110">PARAMETERS</span></span>

### <span data-ttu-id="b3101-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b3101-111">-AutomationAccountName</span></span>
<span data-ttu-id="b3101-112">Bu cmdlet 'in DSC düğümünü kaldırdığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3101-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="b3101-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3101-113">-DefaultProfile</span></span>
<span data-ttu-id="b3101-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b3101-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3101-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b3101-115">-Force</span></span>
<span data-ttu-id="b3101-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="b3101-116">ps_force</span></span>

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

### <span data-ttu-id="b3101-117">-ID</span><span class="sxs-lookup"><span data-stu-id="b3101-117">-Id</span></span>
<span data-ttu-id="b3101-118">Bu cmdlet 'in kaldırdığı DSC düğümünün benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3101-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b3101-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3101-119">-ResourceGroupName</span></span>
<span data-ttu-id="b3101-120">Bu cmdlet 'in bir DSC düğümünü silme</span><span class="sxs-lookup"><span data-stu-id="b3101-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="b3101-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="b3101-121">-Confirm</span></span>
<span data-ttu-id="b3101-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b3101-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3101-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3101-123">-WhatIf</span></span>
<span data-ttu-id="b3101-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b3101-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3101-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b3101-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3101-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3101-126">CommonParameters</span></span>
<span data-ttu-id="b3101-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3101-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3101-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3101-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3101-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3101-129">INPUTS</span></span>

### <span data-ttu-id="b3101-130">System. Guid</span><span class="sxs-lookup"><span data-stu-id="b3101-130">System.Guid</span></span>

### <span data-ttu-id="b3101-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b3101-131">System.String</span></span>

## <span data-ttu-id="b3101-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3101-132">OUTPUTS</span></span>

### <span data-ttu-id="b3101-133">Microsoft. Azure. Commands. Automation. model. DscNode</span><span class="sxs-lookup"><span data-stu-id="b3101-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="b3101-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3101-134">NOTES</span></span>

## <span data-ttu-id="b3101-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3101-135">RELATED LINKS</span></span>

[<span data-ttu-id="b3101-136">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b3101-136">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="b3101-137">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b3101-137">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="b3101-138">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b3101-138">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)


