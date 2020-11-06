---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/register-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
ms.openlocfilehash: 567ac6012465508fbaf03d603a79d2abb04ed6c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591441"
---
# <span data-ttu-id="9f80f-101">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="9f80f-101">Register-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="9f80f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f80f-102">SYNOPSIS</span></span>
<span data-ttu-id="9f80f-103">Bir Otomasyon hesabı için bir Azure sanal makinesini DSC düğümü olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="9f80f-103">Registers an Azure virtual machine as a DSC node for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f80f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f80f-104">SYNTAX</span></span>

```
Register-AzureRmAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f80f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f80f-105">DESCRIPTION</span></span>
<span data-ttu-id="9f80f-106">**Register-AzureRmAutomationDscNode** cmdlet 'i bir Azure Otomasyonu hesabında bir Mac sanal MAKINESINI bir APS Istenen durum YAPıLANDıRMASı (DSC) düğümü olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="9f80f-106">The **Register-AzureRmAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span>

## <span data-ttu-id="9f80f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f80f-107">EXAMPLES</span></span>

### <span data-ttu-id="9f80f-108">Örnek 1: Azure sanal makinesini Azure DSC düğümü olarak kaydettirme</span><span class="sxs-lookup"><span data-stu-id="9f80f-108">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="9f80f-109">Bu komut VirtualMachine01 adındaki bir Azure sanal makinesini Contoso17 adındaki Otomasyon hesabında DSC düğümü olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="9f80f-109">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="9f80f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f80f-110">PARAMETERS</span></span>

### <span data-ttu-id="9f80f-111">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="9f80f-111">-ActionAfterReboot</span></span>
<span data-ttu-id="9f80f-112">Yeniden başlatıldıktan sonra sanal makinenin aldığı eylemi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f80f-112">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="9f80f-113">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="9f80f-113">Valid values are:</span></span> 
- <span data-ttu-id="9f80f-114">Devam yapılandırması</span><span class="sxs-lookup"><span data-stu-id="9f80f-114">ContinueConfiguration</span></span> 
- <span data-ttu-id="9f80f-115">Durdurma yapılandırması</span><span class="sxs-lookup"><span data-stu-id="9f80f-115">StopConfiguration</span></span>

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

### <span data-ttu-id="9f80f-116">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="9f80f-116">-AllowModuleOverwrite</span></span>
<span data-ttu-id="9f80f-117">Bu DSC düğümünün Azure Otomasyonu DSC çekme sunucusundan İndirilme yeni yapılandırmaların, var olan modüllerin hedef düğümde var olan modülleri değiştirip değiştirmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f80f-117">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="9f80f-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9f80f-118">-AutomationAccountName</span></span>
<span data-ttu-id="9f80f-119">Bu cmdlet 'in sanal makine kaydettiğinde bir Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f80f-119">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="9f80f-120">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="9f80f-120">-AzureVMLocation</span></span>
<span data-ttu-id="9f80f-121">Bu cmdlet 'in sanal makineyi kaydeden konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f80f-121">Specifies the location in which this cmdlet registers a virtual machine.</span></span>
<span data-ttu-id="9f80f-122">Geçerli konumları almak için Get-AzureRMLocation cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9f80f-122">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

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

### <span data-ttu-id="9f80f-123">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="9f80f-123">-AzureVMName</span></span>
<span data-ttu-id="9f80f-124">Bu cmdlet 'in yönetim için kaydettirkullandığı Azure sanal makinesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f80f-124">Specifies the name of the Azure virtual machine that this cmdlet registers for management.</span></span>

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

### <span data-ttu-id="9f80f-125">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9f80f-125">-AzureVMResourceGroup</span></span>
<span data-ttu-id="9f80f-126">Bu cmdlet 'in kaydettiğinde Azure sanal makinesinin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f80f-126">Specifies the name of the resource group of the Azure virtual machine that this cmdlet registers.</span></span>

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

### <span data-ttu-id="9f80f-127">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="9f80f-127">-ConfigurationMode</span></span>
<span data-ttu-id="9f80f-128">DSC yapılandırma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f80f-128">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="9f80f-129">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="9f80f-129">Valid values are:</span></span> 
- <span data-ttu-id="9f80f-130">Applyandmonitörü</span><span class="sxs-lookup"><span data-stu-id="9f80f-130">ApplyAndMonitor</span></span> 
- <span data-ttu-id="9f80f-131">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="9f80f-131">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="9f80f-132">Yalnızca Apply</span><span class="sxs-lookup"><span data-stu-id="9f80f-132">ApplyOnly</span></span>

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

### <span data-ttu-id="9f80f-133">-Configurationmodeftalep</span><span class="sxs-lookup"><span data-stu-id="9f80f-133">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="9f80f-134">DSC 'nin arka plan uygulamasının hedef düğümdeki geçerli yapılandırmayı uygulama girişimlerinin dakika cinsinden süresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f80f-134">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="9f80f-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f80f-135">-DefaultProfile</span></span>
<span data-ttu-id="9f80f-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9f80f-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f80f-137">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="9f80f-137">-NodeConfigurationName</span></span>
<span data-ttu-id="9f80f-138">Bu cmdlet 'in sanal makineyi Azure Automation DSC 'den çekme için yapılandırdığını düğümün yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f80f-138">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="9f80f-139">-Rebootnodeıfgerekli</span><span class="sxs-lookup"><span data-stu-id="9f80f-139">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="9f80f-140">Gerekirse sanal makinenin yeniden etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f80f-140">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="9f80f-141">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="9f80f-141">-RefreshFrequencyMins</span></span>
<span data-ttu-id="9f80f-142">Yerel Configuration Manager 'ın en son düğüm yapılandırmasını indirmek için Azure Otomasyonu DSC istek sunucusuyla iletişim kurduğunda frekansı dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f80f-142">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="9f80f-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f80f-143">-ResourceGroupName</span></span>
<span data-ttu-id="9f80f-144">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f80f-144">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9f80f-145">Bu cmdlet 'in bir sanal makineyi kaydeden Otomasyon hesabı, bu parametrenin belirttiği kaynak grubuna aittir.</span><span class="sxs-lookup"><span data-stu-id="9f80f-145">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9f80f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f80f-146">CommonParameters</span></span>
<span data-ttu-id="9f80f-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f80f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f80f-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f80f-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f80f-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f80f-149">INPUTS</span></span>

### <span data-ttu-id="9f80f-150">System. String</span><span class="sxs-lookup"><span data-stu-id="9f80f-150">System.String</span></span>

### <span data-ttu-id="9f80f-151">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9f80f-151">System.Int32</span></span>

### <span data-ttu-id="9f80f-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9f80f-152">System.Boolean</span></span>

## <span data-ttu-id="9f80f-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f80f-153">OUTPUTS</span></span>

### <span data-ttu-id="9f80f-154">System. void</span><span class="sxs-lookup"><span data-stu-id="9f80f-154">System.Void</span></span>

## <span data-ttu-id="9f80f-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f80f-155">NOTES</span></span>

## <span data-ttu-id="9f80f-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f80f-156">RELATED LINKS</span></span>

[<span data-ttu-id="9f80f-157">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="9f80f-157">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="9f80f-158">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="9f80f-158">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)

[<span data-ttu-id="9f80f-159">Unregister-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="9f80f-159">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)


