---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
ms.openlocfilehash: 6fa6b5b9bd7d73c0a2f5ea42b7878e9ce00cf6ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595114"
---
# <span data-ttu-id="4209e-101">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="4209e-101">Get-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="4209e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4209e-102">SYNOPSIS</span></span>
<span data-ttu-id="4209e-103">Otomasyondan DSC düğümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="4209e-103">Gets DSC nodes from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4209e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4209e-104">SYNTAX</span></span>

### <span data-ttu-id="4209e-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4209e-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4209e-106">Byıd</span><span class="sxs-lookup"><span data-stu-id="4209e-106">ById</span></span>
```
Get-AzureRmAutomationDscNode -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4209e-107">ByName</span><span class="sxs-lookup"><span data-stu-id="4209e-107">ByName</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4209e-108">ByNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="4209e-108">ByNodeConfiguration</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -NodeConfigurationName <String>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4209e-109">ByConfiguration</span><span class="sxs-lookup"><span data-stu-id="4209e-109">ByConfiguration</span></span>
```
Get-AzureRmAutomationDscNode -ConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4209e-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="4209e-110">DESCRIPTION</span></span>
<span data-ttu-id="4209e-111">**Get-AzureRmAutomationDscNode** cmdlet 'i, Mac otomasyonundan APS Istenen durum yapılandırma (DSC) düğümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="4209e-111">The **Get-AzureRmAutomationDscNode** cmdlet gets APS Desired State Configuration (DSC) nodes from Azure Automation.</span></span>

## <span data-ttu-id="4209e-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4209e-112">EXAMPLES</span></span>

### <span data-ttu-id="4209e-113">Örnek 1: tüm DSC düğümlerini alma</span><span class="sxs-lookup"><span data-stu-id="4209e-113">Example 1: Get all DSC nodes</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="4209e-114">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm DSC düğümlerinin meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="4209e-114">This command gets metadata for all DSC nodes in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="4209e-115">Örnek 2: DSC yapılandırması için tüm DSC düğümlerini alma</span><span class="sxs-lookup"><span data-stu-id="4209e-115">Example 2: Get all DSC nodes for a DSC configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="4209e-116">Bu komut, DSC yapılandırması Contosoyapılandırması tarafından oluşturulan bir DSC düğüm yapılandırmasıyla eşlenmiş olan Contoso17 adlı Otomasyon hesabındaki tüm DSC düğümlerine ait meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="4209e-116">This command gets metadata for all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration which was generated by DSC configuration ContosoConfiguration.</span></span>

### <span data-ttu-id="4209e-117">Örnek 3: KIMLIĞE göre DSC düğümü alma</span><span class="sxs-lookup"><span data-stu-id="4209e-117">Example 3: Get a DSC node by ID</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="4209e-118">Bu komut, Contoso17 adlı Otomasyon hesabında belirtilen KIMLIĞE sahip bir DSC düğümündeki meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="4209e-118">This command gets metadata on a DSC node with the specified ID in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="4209e-119">Örnek 4: ada göre bir DSC düğümü alma</span><span class="sxs-lookup"><span data-stu-id="4209e-119">Example 4: Get a DSC node by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

<span data-ttu-id="4209e-120">Bu komut, Contoso17 adındaki Otomasyon hesabındaki Computer14 adındaki bir DSC düğümündeki meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="4209e-120">This command gets metadata on a DSC node with the name Computer14 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="4209e-121">Örnek 5: DSC düğüm yapılandırmasına eşlenmiş tüm DSC düğümlerini alma</span><span class="sxs-lookup"><span data-stu-id="4209e-121">Example 5: Get all DSC nodes mapped to a DSC node configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="4209e-122">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm DSC düğümlerinde, ContosoConfiguration. webserver adlı bir DSC düğüm yapılandırmasına eşlenmiş tüm DSC düğümlerinde meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="4209e-122">This command gets metadata on all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration named ContosoConfiguration.webserver.</span></span>

## <span data-ttu-id="4209e-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4209e-123">PARAMETERS</span></span>

### <span data-ttu-id="4209e-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4209e-124">-AutomationAccountName</span></span>
<span data-ttu-id="4209e-125">Bu cmdlet 'in aldığı DSC düğümlerini içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4209e-125">Specifies the name of the Automation account that contains the DSC nodes that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4209e-126">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="4209e-126">-ConfigurationName</span></span>
<span data-ttu-id="4209e-127">DSC yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4209e-127">Specifies the name of a DSC configuration.</span></span>
<span data-ttu-id="4209e-128">Bu cmdlet, bu parametrenin belirttiği yapılandırmadan oluşturulan düğüm yapılandırmalarıyla eşleşen DSC düğümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="4209e-128">This cmdlet gets DSC nodes that match the node configurations generated from the configuration that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4209e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4209e-129">-DefaultProfile</span></span>
<span data-ttu-id="4209e-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4209e-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4209e-131">-ID</span><span class="sxs-lookup"><span data-stu-id="4209e-131">-Id</span></span>
<span data-ttu-id="4209e-132">Bu cmdlet 'in aldığı DSC düğümünün benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4209e-132">Specifies the unique ID of the DSC node that this cmdlet gets.</span></span>

```yaml
Type: Guid
Parameter Sets: ById
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4209e-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="4209e-133">-Name</span></span>
<span data-ttu-id="4209e-134">Bu cmdlet 'in aldığı DSC düğümünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4209e-134">Specifies the name of a DSC node that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: NodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4209e-135">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="4209e-135">-NodeConfigurationName</span></span>
<span data-ttu-id="4209e-136">Bu cmdlet 'in aldığı düğüm yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4209e-136">Specifies the name of a node configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4209e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4209e-137">-ResourceGroupName</span></span>
<span data-ttu-id="4209e-138">Bu cmdlet 'in DSC düğümlerini aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4209e-138">Specifies the name of a resource group in which this cmdlet gets DSC nodes.</span></span>

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

### <span data-ttu-id="4209e-139">-Durum</span><span class="sxs-lookup"><span data-stu-id="4209e-139">-Status</span></span>
<span data-ttu-id="4209e-140">Bu cmdlet 'in aldığı DSC düğümlerinin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4209e-140">Specifies the status of the DSC nodes that this cmdlet gets.</span></span>
<span data-ttu-id="4209e-141">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="4209e-141">Valid values are:</span></span> 

- <span data-ttu-id="4209e-142">Uyumlu</span><span class="sxs-lookup"><span data-stu-id="4209e-142">Compliant</span></span> 
- <span data-ttu-id="4209e-143">NotUyumlu</span><span class="sxs-lookup"><span data-stu-id="4209e-143">NotCompliant</span></span>
- <span data-ttu-id="4209e-144">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="4209e-144">Failed</span></span>
- <span data-ttu-id="4209e-145">Bekley</span><span class="sxs-lookup"><span data-stu-id="4209e-145">Pending</span></span> 
- <span data-ttu-id="4209e-146">Alınmazsa</span><span class="sxs-lookup"><span data-stu-id="4209e-146">Received</span></span>
- <span data-ttu-id="4209e-147">Katılımcıya</span><span class="sxs-lookup"><span data-stu-id="4209e-147">Unresponsive</span></span>

```yaml
Type: DscNodeStatus
Parameter Sets: ByAll, ByName, ByNodeConfiguration
Aliases: 
Accepted values: Compliant, NotCompliant, Failed, Pending, Received, Unresponsive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4209e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4209e-148">CommonParameters</span></span>
<span data-ttu-id="4209e-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4209e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4209e-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4209e-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4209e-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4209e-151">INPUTS</span></span>

### <span data-ttu-id="4209e-152">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4209e-152">None</span></span>
<span data-ttu-id="4209e-153">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4209e-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4209e-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4209e-154">OUTPUTS</span></span>

### <span data-ttu-id="4209e-155">Microsoft. Azure. Commands. Automation. model. DscNode</span><span class="sxs-lookup"><span data-stu-id="4209e-155">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="4209e-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4209e-156">NOTES</span></span>

## <span data-ttu-id="4209e-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4209e-157">RELATED LINKS</span></span>

[<span data-ttu-id="4209e-158">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="4209e-158">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="4209e-159">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="4209e-159">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)

[<span data-ttu-id="4209e-160">Unregister-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="4209e-160">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)


