---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
ms.openlocfilehash: 9d4efbccffeae2654b5be6d6db8635e588fd87f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761628"
---
# <span data-ttu-id="b2f38-101">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b2f38-101">Get-AzAutomationDscNode</span></span>

## <span data-ttu-id="b2f38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2f38-102">SYNOPSIS</span></span>
<span data-ttu-id="b2f38-103">Otomasyondan DSC düğümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="b2f38-103">Gets DSC nodes from Automation.</span></span>

## <span data-ttu-id="b2f38-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b2f38-104">SYNTAX</span></span>

### <span data-ttu-id="b2f38-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b2f38-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2f38-106">Byıd</span><span class="sxs-lookup"><span data-stu-id="b2f38-106">ById</span></span>
```
Get-AzAutomationDscNode -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2f38-107">ByName</span><span class="sxs-lookup"><span data-stu-id="b2f38-107">ByName</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2f38-108">ByNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2f38-108">ByNodeConfiguration</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] -NodeConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2f38-109">ByConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2f38-109">ByConfiguration</span></span>
```
Get-AzAutomationDscNode -ConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2f38-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="b2f38-110">DESCRIPTION</span></span>
<span data-ttu-id="b2f38-111">**Get-AzAutomationDscNode** cmdlet 'i,%</span><span class="sxs-lookup"><span data-stu-id="b2f38-111">The **Get-AzAutomationDscNode** cmdlet gets APS Desired State Configuration (DSC) nodes from Azure Automation.</span></span>

## <span data-ttu-id="b2f38-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b2f38-112">EXAMPLES</span></span>

### <span data-ttu-id="b2f38-113">Örnek 1: tüm DSC düğümlerini alma</span><span class="sxs-lookup"><span data-stu-id="b2f38-113">Example 1: Get all DSC nodes</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="b2f38-114">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm DSC düğümlerinin meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="b2f38-114">This command gets metadata for all DSC nodes in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="b2f38-115">Örnek 2: DSC yapılandırması için tüm DSC düğümlerini alma</span><span class="sxs-lookup"><span data-stu-id="b2f38-115">Example 2: Get all DSC nodes for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="b2f38-116">Bu komut, DSC yapılandırması Contosoyapılandırması tarafından oluşturulan bir DSC düğüm yapılandırmasıyla eşlenmiş olan Contoso17 adlı Otomasyon hesabındaki tüm DSC düğümlerine ait meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="b2f38-116">This command gets metadata for all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration which was generated by DSC configuration ContosoConfiguration.</span></span>

### <span data-ttu-id="b2f38-117">Örnek 3: KIMLIĞE göre DSC düğümü alma</span><span class="sxs-lookup"><span data-stu-id="b2f38-117">Example 3: Get a DSC node by ID</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="b2f38-118">Bu komut, Contoso17 adlı Otomasyon hesabında belirtilen KIMLIĞE sahip bir DSC düğümündeki meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="b2f38-118">This command gets metadata on a DSC node with the specified ID in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="b2f38-119">Örnek 4: ada göre bir DSC düğümü alma</span><span class="sxs-lookup"><span data-stu-id="b2f38-119">Example 4: Get a DSC node by name</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

<span data-ttu-id="b2f38-120">Bu komut, Contoso17 adındaki Otomasyon hesabındaki Computer14 adındaki bir DSC düğümündeki meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="b2f38-120">This command gets metadata on a DSC node with the name Computer14 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="b2f38-121">Örnek 5: DSC düğüm yapılandırmasına eşlenmiş tüm DSC düğümlerini alma</span><span class="sxs-lookup"><span data-stu-id="b2f38-121">Example 5: Get all DSC nodes mapped to a DSC node configuration</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="b2f38-122">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm DSC düğümlerinde, ContosoConfiguration. webserver adlı bir DSC düğüm yapılandırmasına eşlenmiş tüm DSC düğümlerinde meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="b2f38-122">This command gets metadata on all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration named ContosoConfiguration.webserver.</span></span>

## <span data-ttu-id="b2f38-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b2f38-123">PARAMETERS</span></span>

### <span data-ttu-id="b2f38-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b2f38-124">-AutomationAccountName</span></span>
<span data-ttu-id="b2f38-125">Bu cmdlet 'in aldığı DSC düğümlerini içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2f38-125">Specifies the name of the Automation account that contains the DSC nodes that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b2f38-126">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="b2f38-126">-ConfigurationName</span></span>
<span data-ttu-id="b2f38-127">DSC yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2f38-127">Specifies the name of a DSC configuration.</span></span>
<span data-ttu-id="b2f38-128">Bu cmdlet, bu parametrenin belirttiği yapılandırmadan oluşturulan düğüm yapılandırmalarıyla eşleşen DSC düğümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="b2f38-128">This cmdlet gets DSC nodes that match the node configurations generated from the configuration that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2f38-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2f38-129">-DefaultProfile</span></span>
<span data-ttu-id="b2f38-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b2f38-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2f38-131">-ID</span><span class="sxs-lookup"><span data-stu-id="b2f38-131">-Id</span></span>
<span data-ttu-id="b2f38-132">Bu cmdlet 'in aldığı DSC düğümünün benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2f38-132">Specifies the unique ID of the DSC node that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2f38-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="b2f38-133">-Name</span></span>
<span data-ttu-id="b2f38-134">Bu cmdlet 'in aldığı DSC düğümünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2f38-134">Specifies the name of a DSC node that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2f38-135">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="b2f38-135">-NodeConfigurationName</span></span>
<span data-ttu-id="b2f38-136">Bu cmdlet 'in aldığı düğüm yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2f38-136">Specifies the name of a node configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2f38-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2f38-137">-ResourceGroupName</span></span>
<span data-ttu-id="b2f38-138">Bu cmdlet 'in DSC düğümlerini aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2f38-138">Specifies the name of a resource group in which this cmdlet gets DSC nodes.</span></span>

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

### <span data-ttu-id="b2f38-139">-Durum</span><span class="sxs-lookup"><span data-stu-id="b2f38-139">-Status</span></span>
<span data-ttu-id="b2f38-140">Bu cmdlet 'in aldığı DSC düğümlerinin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2f38-140">Specifies the status of the DSC nodes that this cmdlet gets.</span></span>
<span data-ttu-id="b2f38-141">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="b2f38-141">Valid values are:</span></span> 
- <span data-ttu-id="b2f38-142">Uyumlu</span><span class="sxs-lookup"><span data-stu-id="b2f38-142">Compliant</span></span> 
- <span data-ttu-id="b2f38-143">NotUyumlu</span><span class="sxs-lookup"><span data-stu-id="b2f38-143">NotCompliant</span></span>
- <span data-ttu-id="b2f38-144">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="b2f38-144">Failed</span></span>
- <span data-ttu-id="b2f38-145">Bekley</span><span class="sxs-lookup"><span data-stu-id="b2f38-145">Pending</span></span> 
- <span data-ttu-id="b2f38-146">Alınmazsa</span><span class="sxs-lookup"><span data-stu-id="b2f38-146">Received</span></span>
- <span data-ttu-id="b2f38-147">Katılımcıya</span><span class="sxs-lookup"><span data-stu-id="b2f38-147">Unresponsive</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.DscNodeStatus
Parameter Sets: ByAll, ByName, ByNodeConfiguration
Aliases:
Accepted values: Compliant, NotCompliant, Failed, Pending, Received, Unresponsive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2f38-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2f38-148">CommonParameters</span></span>
<span data-ttu-id="b2f38-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b2f38-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2f38-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2f38-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2f38-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b2f38-151">INPUTS</span></span>

### <span data-ttu-id="b2f38-152">System. Guid</span><span class="sxs-lookup"><span data-stu-id="b2f38-152">System.Guid</span></span>

### <span data-ttu-id="b2f38-153">System. String</span><span class="sxs-lookup"><span data-stu-id="b2f38-153">System.String</span></span>

## <span data-ttu-id="b2f38-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b2f38-154">OUTPUTS</span></span>

### <span data-ttu-id="b2f38-155">Microsoft. Azure. Commands. Automation. model. DscNode</span><span class="sxs-lookup"><span data-stu-id="b2f38-155">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="b2f38-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b2f38-156">NOTES</span></span>

## <span data-ttu-id="b2f38-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b2f38-157">RELATED LINKS</span></span>

[<span data-ttu-id="b2f38-158">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b2f38-158">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="b2f38-159">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b2f38-159">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="b2f38-160">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b2f38-160">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)

