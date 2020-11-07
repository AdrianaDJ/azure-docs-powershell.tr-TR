---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
ms.openlocfilehash: c006c06d03e1f1c120ed62f38ea8b3e451d8fa21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764672"
---
# <span data-ttu-id="3e984-101">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3e984-101">Set-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="3e984-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e984-102">SYNOPSIS</span></span>
<span data-ttu-id="3e984-103">SAP sistemlerini izlemeye yönelik desteği destekler.</span><span class="sxs-lookup"><span data-stu-id="3e984-103">Enables support for monitoring for SAP systems.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e984-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e984-104">SYNTAX</span></span>

```
Set-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e984-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e984-105">DESCRIPTION</span></span>
<span data-ttu-id="3e984-106">**Set-AzureRmVMAEMExtension** cmdlet 'i sanal makinenin yapılandırmasını güncelleştirerek sanal MAKINEDE yüklü SAP sistemlerini izlemeye yönelik desteği etkinleştirir veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3e984-106">The **Set-AzureRmVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="3e984-107">Cmdlet, performans verilerini toplayan ve SAP sistemi için bulunabilir kılan Azure Enhanced Monitoring (AEM) uzantısını yükler.</span><span class="sxs-lookup"><span data-stu-id="3e984-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="3e984-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e984-108">EXAMPLES</span></span>

### <span data-ttu-id="3e984-109">Örnek 1: AEM uzantısını kullanma</span><span class="sxs-lookup"><span data-stu-id="3e984-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="3e984-110">Bu komut, Contoso sunucusu adındaki sanal makineyi AEM uzantısını kullanacak şekilde yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="3e984-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="3e984-111">Komut, stddepolama adlı depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e984-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="3e984-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e984-112">PARAMETERS</span></span>

### <span data-ttu-id="3e984-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e984-113">-DefaultProfile</span></span>
<span data-ttu-id="3e984-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3e984-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e984-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="3e984-115">-EnableWAD</span></span>
<span data-ttu-id="3e984-116">Bu parametre sağlanmışsa, commandme bu sanal makine için Windows Azure tanılamasını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="3e984-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

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

### <span data-ttu-id="3e984-117">-OSType</span><span class="sxs-lookup"><span data-stu-id="3e984-117">-OSType</span></span>
<span data-ttu-id="3e984-118">İşletim sistemi diskinin işletim sisteminin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e984-118">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="3e984-119">İşletim sistemi diskinin türü yoksa, bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3e984-119">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="3e984-120">Bu parametre için kabul edilebilir değerler: Windows ve Linux.</span><span class="sxs-lookup"><span data-stu-id="3e984-120">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="3e984-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e984-121">-ResourceGroupName</span></span>
<span data-ttu-id="3e984-122">Bu cmdlet 'in değiştirdiği sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e984-122">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3e984-123">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="3e984-123">-SkipStorage</span></span>
<span data-ttu-id="3e984-124">Bu cmdlet 'in depolama yapılandırmasını aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e984-124">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="3e984-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="3e984-125">-VMName</span></span>
<span data-ttu-id="3e984-126">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e984-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="3e984-127">Bu cmdlet, bu parametrenin belirttiği sanal makine için AEM uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="3e984-127">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="3e984-128">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3e984-128">-WADStorageAccountName</span></span>
<span data-ttu-id="3e984-129">Bu cmdlet 'in LinuxDiagnostics veya IaaSDiagnostics uzantısını yapılandırmak için kullandığı depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e984-129">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="3e984-130">Sanal makine standart depolama hesabı kullanmazsa bu parametre için bir değer belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3e984-130">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="3e984-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e984-131">CommonParameters</span></span>
<span data-ttu-id="3e984-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e984-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e984-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e984-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e984-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e984-134">INPUTS</span></span>

### <span data-ttu-id="3e984-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3e984-135">System.String</span></span>

## <span data-ttu-id="3e984-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e984-136">OUTPUTS</span></span>

### <span data-ttu-id="3e984-137">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3e984-137">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3e984-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e984-138">NOTES</span></span>

## <span data-ttu-id="3e984-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e984-139">RELATED LINKS</span></span>

[<span data-ttu-id="3e984-140">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3e984-140">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="3e984-141">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3e984-141">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="3e984-142">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3e984-142">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


