---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: b476254d5b9236aa95a30832499aca65a8a110c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268564"
---
# <span data-ttu-id="70ac4-101">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="70ac4-101">Set-AzVMAEMExtension</span></span>

## <span data-ttu-id="70ac4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70ac4-102">SYNOPSIS</span></span>
<span data-ttu-id="70ac4-103">SAP sistemlerini izlemeye yönelik desteği destekler.</span><span class="sxs-lookup"><span data-stu-id="70ac4-103">Enables support for monitoring for SAP systems.</span></span>

## <span data-ttu-id="70ac4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="70ac4-104">SYNTAX</span></span>

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [-NoWait]
 [-SetAccessToIndividualResources] [-InstallNewExtension] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70ac4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="70ac4-105">DESCRIPTION</span></span>
<span data-ttu-id="70ac4-106">**Set-AzVMAEMExtension** cmdlet 'i sanal makinenin yapılandırmasını güncelleştirerek sanal MAKINEDE yüklü SAP sistemlerini izlemeye yönelik desteği etkinleştirir veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="70ac4-106">The **Set-AzVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="70ac4-107">Cmdlet, performans verilerini toplayan ve SAP sistemi için bulunabilir kılan Azure Enhanced Monitoring (AEM) uzantısını yükler.</span><span class="sxs-lookup"><span data-stu-id="70ac4-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="70ac4-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="70ac4-108">EXAMPLES</span></span>

### <span data-ttu-id="70ac4-109">Örnek 1: AEM uzantısını kullanma</span><span class="sxs-lookup"><span data-stu-id="70ac4-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="70ac4-110">Bu komut, Contoso sunucusu adındaki sanal makineyi AEM uzantısını kullanacak şekilde yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="70ac4-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="70ac4-111">Komut, stddepolama adlı depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="70ac4-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="70ac4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="70ac4-112">PARAMETERS</span></span>

### <span data-ttu-id="70ac4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70ac4-113">-DefaultProfile</span></span>
<span data-ttu-id="70ac4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="70ac4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70ac4-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="70ac4-115">-EnableWAD</span></span>
<span data-ttu-id="70ac4-116">Bu parametre sağlanmışsa, commandme bu sanal makine için Windows Azure tanılamasını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="70ac4-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70ac4-117">-Installnewextension</span><span class="sxs-lookup"><span data-stu-id="70ac4-117">-InstallNewExtension</span></span>
<span data-ttu-id="70ac4-118">SAP için yeni VM Uzantısı 'nı yükleyin.</span><span class="sxs-lookup"><span data-stu-id="70ac4-118">Install the new VM Extension for SAP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70ac4-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="70ac4-119">-NoWait</span></span>
<span data-ttu-id="70ac4-120">İşlemi başlatır ve işlem tamamlanmadan hemen döner.</span><span class="sxs-lookup"><span data-stu-id="70ac4-120">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="70ac4-121">İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.</span><span class="sxs-lookup"><span data-stu-id="70ac4-121">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="70ac4-122">-OSType</span><span class="sxs-lookup"><span data-stu-id="70ac4-122">-OSType</span></span>
<span data-ttu-id="70ac4-123">İşletim sistemi diskinin işletim sisteminin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="70ac4-123">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="70ac4-124">İşletim sistemi diskinin türü yoksa, bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="70ac4-124">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="70ac4-125">Bu parametre için kabul edilebilir değerler: Windows ve Linux.</span><span class="sxs-lookup"><span data-stu-id="70ac4-125">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70ac4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70ac4-126">-ResourceGroupName</span></span>
<span data-ttu-id="70ac4-127">Bu cmdlet 'in değiştirdiği sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="70ac4-127">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="70ac4-128">-Setaccesstobireyalresources</span><span class="sxs-lookup"><span data-stu-id="70ac4-128">-SetAccessToIndividualResources</span></span>
<span data-ttu-id="70ac4-129">VM kimliğinin erişimini tek tek kaynaklara ayarlar (örneğin, kaynak grubu).</span><span class="sxs-lookup"><span data-stu-id="70ac4-129">Sets the access of the VM identity to the individual resources, e.g. data disks instead of the complete resource group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70ac4-130">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="70ac4-130">-SkipStorage</span></span>
<span data-ttu-id="70ac4-131">Bu cmdlet 'in depolama yapılandırmasını aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="70ac4-131">Indicates that this cmdlet skips configuration of storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70ac4-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="70ac4-132">-VMName</span></span>
<span data-ttu-id="70ac4-133">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="70ac4-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="70ac4-134">Bu cmdlet, bu parametrenin belirttiği sanal makine için AEM uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="70ac4-134">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70ac4-135">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="70ac4-135">-WADStorageAccountName</span></span>
<span data-ttu-id="70ac4-136">Bu cmdlet 'in LinuxDiagnostics veya IaaSDiagnostics uzantısını yapılandırmak için kullandığı depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="70ac4-136">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="70ac4-137">Sanal makine standart depolama hesabı kullanmazsa bu parametre için bir değer belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="70ac4-137">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70ac4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70ac4-138">CommonParameters</span></span>
<span data-ttu-id="70ac4-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="70ac4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70ac4-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="70ac4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70ac4-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="70ac4-141">INPUTS</span></span>

### <span data-ttu-id="70ac4-142">System. String</span><span class="sxs-lookup"><span data-stu-id="70ac4-142">System.String</span></span>

## <span data-ttu-id="70ac4-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="70ac4-143">OUTPUTS</span></span>

### <span data-ttu-id="70ac4-144">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="70ac4-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="70ac4-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="70ac4-145">NOTES</span></span>

## <span data-ttu-id="70ac4-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="70ac4-146">RELATED LINKS</span></span>

[<span data-ttu-id="70ac4-147">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="70ac4-147">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="70ac4-148">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="70ac4-148">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="70ac4-149">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="70ac4-149">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


