---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
ms.openlocfilehash: 663573e7f4e111880c5ed0014dcad18480f665ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762390"
---
# <span data-ttu-id="8b4a2-101">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="8b4a2-101">Set-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="8b4a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b4a2-102">SYNOPSIS</span></span>
<span data-ttu-id="8b4a2-103">DSC düğümünün eşlendiği düğüm yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8b4a2-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b4a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b4a2-104">SYNTAX</span></span>

```
Set-AzureRmAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b4a2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b4a2-105">DESCRIPTION</span></span>
<span data-ttu-id="8b4a2-106">**Set-AzureRmAutomationDscNode** cmdlet 'ı, APS</span><span class="sxs-lookup"><span data-stu-id="8b4a2-106">The **Set-AzureRmAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="8b4a2-107">Azure Otomasyonu, DSC düğüm yapılandırmasını yönetilen nesne biçimi (MOF) yapılandırma belgesi olarak depolar.</span><span class="sxs-lookup"><span data-stu-id="8b4a2-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="8b4a2-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b4a2-108">EXAMPLES</span></span>

### <span data-ttu-id="8b4a2-109">Örnek 1: düğüm yapılandırma eşlemesini değiştirme</span><span class="sxs-lookup"><span data-stu-id="8b4a2-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzureRmAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="8b4a2-110">Bu komut, contoso. NodeConfiguration01 adlı düğüm yapılandırmasını belirtilen GUID 'ye sahip düğüme atar.</span><span class="sxs-lookup"><span data-stu-id="8b4a2-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="8b4a2-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b4a2-111">PARAMETERS</span></span>

### <span data-ttu-id="8b4a2-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8b4a2-112">-AutomationAccountName</span></span>
<span data-ttu-id="8b4a2-113">Bu cmdlet 'in yapılandırmayı değiştirdiği DSC düğümünü içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b4a2-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="8b4a2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b4a2-114">-DefaultProfile</span></span>
<span data-ttu-id="8b4a2-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8b4a2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b4a2-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8b4a2-116">-Force</span></span>
<span data-ttu-id="8b4a2-117">kullanıcıya onay istemeden çalıştırılacak komutu ps_force.</span><span class="sxs-lookup"><span data-stu-id="8b4a2-117">ps_force the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8b4a2-118">-ID</span><span class="sxs-lookup"><span data-stu-id="8b4a2-118">-Id</span></span>
<span data-ttu-id="8b4a2-119">Bu cmdlet 'in yapılandırmayı değiştirdiği DSC düğümünün benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b4a2-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b4a2-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8b4a2-120">-NodeConfigurationName</span></span>
<span data-ttu-id="8b4a2-121">Bu cmdlet 'in düğümü eşlendiği düğüm yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b4a2-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b4a2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b4a2-122">-ResourceGroupName</span></span>
<span data-ttu-id="8b4a2-123">Bu cmdlet 'in DSC düğüm yapılandırmasını değiştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b4a2-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

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

### <span data-ttu-id="8b4a2-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="8b4a2-124">-Confirm</span></span>
<span data-ttu-id="8b4a2-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8b4a2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b4a2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b4a2-126">-WhatIf</span></span>
<span data-ttu-id="8b4a2-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8b4a2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b4a2-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8b4a2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b4a2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b4a2-129">CommonParameters</span></span>
<span data-ttu-id="8b4a2-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b4a2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b4a2-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b4a2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b4a2-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b4a2-132">INPUTS</span></span>

### <span data-ttu-id="8b4a2-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8b4a2-133">None</span></span>
<span data-ttu-id="8b4a2-134">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="8b4a2-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8b4a2-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b4a2-135">OUTPUTS</span></span>

### <span data-ttu-id="8b4a2-136">Microsoft. Azure. Commands. Automation. model. DscNode</span><span class="sxs-lookup"><span data-stu-id="8b4a2-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="8b4a2-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b4a2-137">NOTES</span></span>

## <span data-ttu-id="8b4a2-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b4a2-138">RELATED LINKS</span></span>

[<span data-ttu-id="8b4a2-139">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="8b4a2-139">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="8b4a2-140">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="8b4a2-140">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="8b4a2-141">Unregister-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="8b4a2-141">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)

