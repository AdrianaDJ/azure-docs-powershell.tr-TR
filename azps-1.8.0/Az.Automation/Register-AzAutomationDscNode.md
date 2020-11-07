---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: 5dc2682597be6f05a65bafc38424139e9707578f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761548"
---
# <span data-ttu-id="0b086-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0b086-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="0b086-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b086-102">SYNOPSIS</span></span>
<span data-ttu-id="0b086-103">Bir Otomasyon hesabı için bir Azure sanal makinesini DSC düğümü olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="0b086-103">Registers an Azure virtual machine as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="0b086-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b086-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b086-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b086-105">DESCRIPTION</span></span>
<span data-ttu-id="0b086-106">**Register-AzAutomationDscNode** cmdlet 'i, bir Azure Otomasyonu hesabında bir Azure sanal MAKINESINI bir APS Istenen durum YAPıLANDıRMASı (DSC) düğümü olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="0b086-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span>

## <span data-ttu-id="0b086-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b086-107">EXAMPLES</span></span>

### <span data-ttu-id="0b086-108">Örnek 1: Azure sanal makinesini Azure DSC düğümü olarak kaydettirme</span><span class="sxs-lookup"><span data-stu-id="0b086-108">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="0b086-109">Bu komut VirtualMachine01 adındaki bir Azure sanal makinesini Contoso17 adındaki Otomasyon hesabında DSC düğümü olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="0b086-109">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="0b086-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b086-110">PARAMETERS</span></span>

### <span data-ttu-id="0b086-111">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="0b086-111">-ActionAfterReboot</span></span>
<span data-ttu-id="0b086-112">Yeniden başlatıldıktan sonra sanal makinenin aldığı eylemi belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b086-112">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="0b086-113">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="0b086-113">Valid values are:</span></span> 
- <span data-ttu-id="0b086-114">Devam yapılandırması</span><span class="sxs-lookup"><span data-stu-id="0b086-114">ContinueConfiguration</span></span> 
- <span data-ttu-id="0b086-115">Durdurma yapılandırması</span><span class="sxs-lookup"><span data-stu-id="0b086-115">StopConfiguration</span></span>

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

### <span data-ttu-id="0b086-116">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="0b086-116">-AllowModuleOverwrite</span></span>
<span data-ttu-id="0b086-117">Bu DSC düğümünün Azure Otomasyonu DSC çekme sunucusundan İndirilme yeni yapılandırmaların, var olan modüllerin hedef düğümde var olan modülleri değiştirip değiştirmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b086-117">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="0b086-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0b086-118">-AutomationAccountName</span></span>
<span data-ttu-id="0b086-119">Bu cmdlet 'in sanal makine kaydettiğinde bir Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b086-119">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="0b086-120">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="0b086-120">-AzureVMLocation</span></span>
<span data-ttu-id="0b086-121">Azure VM konumu.</span><span class="sxs-lookup"><span data-stu-id="0b086-121">The Azure VM location.</span></span>

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

### <span data-ttu-id="0b086-122">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="0b086-122">-AzureVMName</span></span>
<span data-ttu-id="0b086-123">Azure Otomasyonu DSC ile yönetim için kaydettiriedilecek Azure sanal makinesinin adı.</span><span class="sxs-lookup"><span data-stu-id="0b086-123">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

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

### <span data-ttu-id="0b086-124">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0b086-124">-AzureVMResourceGroup</span></span>
<span data-ttu-id="0b086-125">Azure VM kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0b086-125">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="0b086-126">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="0b086-126">-ConfigurationMode</span></span>
<span data-ttu-id="0b086-127">DSC yapılandırma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b086-127">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="0b086-128">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="0b086-128">Valid values are:</span></span> 
- <span data-ttu-id="0b086-129">Applyandmonitörü</span><span class="sxs-lookup"><span data-stu-id="0b086-129">ApplyAndMonitor</span></span> 
- <span data-ttu-id="0b086-130">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="0b086-130">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="0b086-131">Yalnızca Apply</span><span class="sxs-lookup"><span data-stu-id="0b086-131">ApplyOnly</span></span>

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

### <span data-ttu-id="0b086-132">-Configurationmodeftalep</span><span class="sxs-lookup"><span data-stu-id="0b086-132">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="0b086-133">DSC 'nin arka plan uygulamasının hedef düğümdeki geçerli yapılandırmayı uygulama girişimlerinin dakika cinsinden süresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b086-133">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="0b086-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b086-134">-DefaultProfile</span></span>
<span data-ttu-id="0b086-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0b086-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b086-136">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="0b086-136">-NodeConfigurationName</span></span>
<span data-ttu-id="0b086-137">Bu cmdlet 'in sanal makineyi Azure Automation DSC 'den çekme için yapılandırdığını düğümün yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b086-137">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="0b086-138">-Rebootnodeıfgerekli</span><span class="sxs-lookup"><span data-stu-id="0b086-138">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="0b086-139">Gerekirse sanal makinenin yeniden etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b086-139">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="0b086-140">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="0b086-140">-RefreshFrequencyMins</span></span>
<span data-ttu-id="0b086-141">Yerel Configuration Manager 'ın en son düğüm yapılandırmasını indirmek için Azure Otomasyonu DSC istek sunucusuyla iletişim kurduğunda frekansı dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b086-141">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="0b086-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b086-142">-ResourceGroupName</span></span>
<span data-ttu-id="0b086-143">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b086-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="0b086-144">Bu cmdlet 'in bir sanal makineyi kaydeden Otomasyon hesabı, bu parametrenin belirttiği kaynak grubuna aittir.</span><span class="sxs-lookup"><span data-stu-id="0b086-144">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0b086-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b086-145">CommonParameters</span></span>
<span data-ttu-id="0b086-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b086-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b086-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b086-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b086-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b086-148">INPUTS</span></span>

### <span data-ttu-id="0b086-149">System. String</span><span class="sxs-lookup"><span data-stu-id="0b086-149">System.String</span></span>

### <span data-ttu-id="0b086-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0b086-150">System.Int32</span></span>

### <span data-ttu-id="0b086-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0b086-151">System.Boolean</span></span>

## <span data-ttu-id="0b086-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b086-152">OUTPUTS</span></span>

### <span data-ttu-id="0b086-153">System. void</span><span class="sxs-lookup"><span data-stu-id="0b086-153">System.Void</span></span>

## <span data-ttu-id="0b086-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b086-154">NOTES</span></span>

## <span data-ttu-id="0b086-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b086-155">RELATED LINKS</span></span>

[<span data-ttu-id="0b086-156">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0b086-156">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="0b086-157">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0b086-157">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="0b086-158">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0b086-158">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


