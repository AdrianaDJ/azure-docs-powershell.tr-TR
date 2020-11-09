---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: e8367d4e291f3cd08cdb1020375cce1741a679c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321838"
---
# <span data-ttu-id="d9493-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="d9493-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="d9493-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9493-102">SYNOPSIS</span></span>
<span data-ttu-id="d9493-103">Windows işletim sistemini çalıştıran bir Azure sanal makinesini bir Otomasyon hesabı için DSC düğümü olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="d9493-103">Registers an Azure virtual machine running Windows OS as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="d9493-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9493-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9493-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9493-105">DESCRIPTION</span></span>
<span data-ttu-id="d9493-106">**Register-AzAutomationDscNode** cmdlet 'i, bir Azure Otomasyonu hesabında bir Azure sanal MAKINESINI bir APS Istenen durum YAPıLANDıRMASı (DSC) düğümü olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="d9493-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span> <span data-ttu-id="d9493-107">Bu cmdlet, Windows işletim sistemini çalıştıran VM 'Leri yalnızca bir hesap için Otomasyon DSC düğümü olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="d9493-107">This cmdlet will only register VMs running Windows OS as an Automation DSC Node for an account.</span></span>

<span data-ttu-id="d9493-108">Bir düğümü farklı bir abonelikteki Otomasyon hesabına kaydetmeniz gerekiyorsa cmdlet 'ler yerine ARM şablonunu kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d9493-108">If you need to register a node to an automation account in a different subscription, you will need to use an ARM template rather than cmdlets.</span></span> <span data-ttu-id="d9493-109">Daha fazla ayrıntı için Azure Otomasyonu [belgelerine](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) bakın.</span><span class="sxs-lookup"><span data-stu-id="d9493-109">See the Azure Automation [documentation](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) for more details.</span></span>

## <span data-ttu-id="d9493-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9493-110">EXAMPLES</span></span>

### <span data-ttu-id="d9493-111">Örnek 1: Azure sanal makinesini Azure DSC düğümü olarak kaydettirme</span><span class="sxs-lookup"><span data-stu-id="d9493-111">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="d9493-112">Bu komut VirtualMachine01 adındaki bir Azure sanal makinesini Contoso17 adındaki Otomasyon hesabında DSC düğümü olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="d9493-112">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="d9493-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9493-113">PARAMETERS</span></span>

### <span data-ttu-id="d9493-114">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="d9493-114">-ActionAfterReboot</span></span>
<span data-ttu-id="d9493-115">Yeniden başlatıldıktan sonra sanal makinenin aldığı eylemi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9493-115">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="d9493-116">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="d9493-116">Valid values are:</span></span> 
- <span data-ttu-id="d9493-117">Devam yapılandırması</span><span class="sxs-lookup"><span data-stu-id="d9493-117">ContinueConfiguration</span></span> 
- <span data-ttu-id="d9493-118">Durdurma yapılandırması</span><span class="sxs-lookup"><span data-stu-id="d9493-118">StopConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ContinueConfiguration, StopConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9493-119">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="d9493-119">-AllowModuleOverwrite</span></span>
<span data-ttu-id="d9493-120">Bu DSC düğümünün Azure Otomasyonu DSC çekme sunucusundan İndirilme yeni yapılandırmaların, var olan modüllerin hedef düğümde var olan modülleri değiştirip değiştirmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9493-120">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9493-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d9493-121">-AutomationAccountName</span></span>
<span data-ttu-id="d9493-122">Bu cmdlet 'in sanal makine kaydettiğinde bir Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9493-122">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="d9493-123">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="d9493-123">-AzureVMLocation</span></span>
<span data-ttu-id="d9493-124">Azure VM konumu.</span><span class="sxs-lookup"><span data-stu-id="d9493-124">The Azure VM location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9493-125">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="d9493-125">-AzureVMName</span></span>
<span data-ttu-id="d9493-126">Azure Otomasyonu DSC ile yönetim için kaydettiriedilecek Azure sanal makinesinin adı.</span><span class="sxs-lookup"><span data-stu-id="d9493-126">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9493-127">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d9493-127">-AzureVMResourceGroup</span></span>
<span data-ttu-id="d9493-128">Azure VM kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d9493-128">The Azure VM resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9493-129">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="d9493-129">-ConfigurationMode</span></span>
<span data-ttu-id="d9493-130">DSC yapılandırma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9493-130">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="d9493-131">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="d9493-131">Valid values are:</span></span> 
- <span data-ttu-id="d9493-132">Applyandmonitörü</span><span class="sxs-lookup"><span data-stu-id="d9493-132">ApplyAndMonitor</span></span> 
- <span data-ttu-id="d9493-133">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="d9493-133">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="d9493-134">Yalnızca Apply</span><span class="sxs-lookup"><span data-stu-id="d9493-134">ApplyOnly</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ApplyAndMonitor, ApplyAndAutocorrect, ApplyOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9493-135">-Configurationmodeftalep</span><span class="sxs-lookup"><span data-stu-id="d9493-135">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="d9493-136">DSC 'nin arka plan uygulamasının hedef düğümdeki geçerli yapılandırmayı uygulama girişimlerinin dakika cinsinden süresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9493-136">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9493-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9493-137">-DefaultProfile</span></span>
<span data-ttu-id="d9493-138">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d9493-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9493-139">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d9493-139">-NodeConfigurationName</span></span>
<span data-ttu-id="d9493-140">Bu cmdlet 'in sanal makineyi Azure Automation DSC 'den çekme için yapılandırdığını düğümün yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9493-140">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9493-141">-Rebootnodeıfgerekli</span><span class="sxs-lookup"><span data-stu-id="d9493-141">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="d9493-142">Gerekirse sanal makinenin yeniden etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9493-142">Specifies whether to restart the virtual machine, if needed.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9493-143">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="d9493-143">-RefreshFrequencyMins</span></span>
<span data-ttu-id="d9493-144">Yerel Configuration Manager 'ın en son düğüm yapılandırmasını indirmek için Azure Otomasyonu DSC istek sunucusuyla iletişim kurduğunda frekansı dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9493-144">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9493-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9493-145">-ResourceGroupName</span></span>
<span data-ttu-id="d9493-146">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9493-146">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d9493-147">Bu cmdlet 'in bir sanal makineyi kaydeden Otomasyon hesabı, bu parametrenin belirttiği kaynak grubuna aittir.</span><span class="sxs-lookup"><span data-stu-id="d9493-147">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9493-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9493-148">CommonParameters</span></span>
<span data-ttu-id="d9493-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9493-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9493-150">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9493-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9493-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9493-151">INPUTS</span></span>

### <span data-ttu-id="d9493-152">System. String</span><span class="sxs-lookup"><span data-stu-id="d9493-152">System.String</span></span>

### <span data-ttu-id="d9493-153">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d9493-153">System.Int32</span></span>

### <span data-ttu-id="d9493-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d9493-154">System.Boolean</span></span>

## <span data-ttu-id="d9493-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9493-155">OUTPUTS</span></span>

### <span data-ttu-id="d9493-156">System. void</span><span class="sxs-lookup"><span data-stu-id="d9493-156">System.Void</span></span>

## <span data-ttu-id="d9493-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9493-157">NOTES</span></span>

## <span data-ttu-id="d9493-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9493-158">RELATED LINKS</span></span>

[<span data-ttu-id="d9493-159">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="d9493-159">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="d9493-160">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="d9493-160">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="d9493-161">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="d9493-161">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


