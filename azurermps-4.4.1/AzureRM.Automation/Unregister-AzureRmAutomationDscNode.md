---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
ms.openlocfilehash: 76de3ad08e6acb0035cfa2a9ca5d353fcbf38033
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764272"
---
# <span data-ttu-id="e750e-101">Unregister-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="e750e-101">Unregister-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="e750e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e750e-102">SYNOPSIS</span></span>
<span data-ttu-id="e750e-103">DSC düğümünü bir Otomasyon hesabıyla yönetimden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e750e-103">Removes a DSC node from management by an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e750e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e750e-104">SYNTAX</span></span>

```
Unregister-AzureRmAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e750e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e750e-105">DESCRIPTION</span></span>
<span data-ttu-id="e750e-106">**Unregister-AzureRmAutomationDscNode** cmdlet 'ı bir APS Istenen durum yapılandırma (DSC) düğümünü, bir Azure Otomasyonu hesabıyla yönetimden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e750e-106">The **Unregister-AzureRmAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="e750e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e750e-107">EXAMPLES</span></span>

### <span data-ttu-id="e750e-108">Örnek 1: Azure DSC düğümünü bir Otomasyon hesabı tarafından yönetimden kaldırma</span><span class="sxs-lookup"><span data-stu-id="e750e-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="e750e-109">Bu komut, belirtilen GUID 'ye sahip DSC düğümünü Contoso17 adlı Otomasyon hesabıyla kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e750e-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="e750e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e750e-110">PARAMETERS</span></span>

### <span data-ttu-id="e750e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e750e-111">-AutomationAccountName</span></span>
<span data-ttu-id="e750e-112">Bu cmdlet 'in DSC düğümünü kaldırdığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e750e-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="e750e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e750e-113">-Force</span></span>
<span data-ttu-id="e750e-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="e750e-114">ps_force</span></span>

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

### <span data-ttu-id="e750e-115">-ID</span><span class="sxs-lookup"><span data-stu-id="e750e-115">-Id</span></span>
<span data-ttu-id="e750e-116">Bu cmdlet 'in kaldırdığı DSC düğümünün benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e750e-116">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e750e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e750e-117">-ResourceGroupName</span></span>
<span data-ttu-id="e750e-118">Bu cmdlet 'in bir DSC düğümünü silme</span><span class="sxs-lookup"><span data-stu-id="e750e-118">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="e750e-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="e750e-119">-Confirm</span></span>
<span data-ttu-id="e750e-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e750e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e750e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e750e-121">-WhatIf</span></span>
<span data-ttu-id="e750e-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e750e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e750e-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e750e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e750e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e750e-124">-DefaultProfile</span></span>
<span data-ttu-id="e750e-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e750e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e750e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e750e-126">CommonParameters</span></span>
<span data-ttu-id="e750e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e750e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e750e-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e750e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e750e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e750e-129">INPUTS</span></span>

## <span data-ttu-id="e750e-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e750e-130">OUTPUTS</span></span>

### <span data-ttu-id="e750e-131">Microsoft. Azure. Commands. Automation. model. DscNode</span><span class="sxs-lookup"><span data-stu-id="e750e-131">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="e750e-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e750e-132">NOTES</span></span>

## <span data-ttu-id="e750e-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e750e-133">RELATED LINKS</span></span>

[<span data-ttu-id="e750e-134">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="e750e-134">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="e750e-135">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="e750e-135">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="e750e-136">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="e750e-136">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)


