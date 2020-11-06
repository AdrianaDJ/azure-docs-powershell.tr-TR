---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
ms.openlocfilehash: 931ed484850654ecebc368ced0b378ce2a40944f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586939"
---
# <span data-ttu-id="f6d22-101">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f6d22-101">Set-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="f6d22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6d22-102">SYNOPSIS</span></span>
<span data-ttu-id="f6d22-103">SAP sistemlerini izlemeye yönelik desteği destekler.</span><span class="sxs-lookup"><span data-stu-id="f6d22-103">Enables support for monitoring for SAP systems.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6d22-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6d22-104">SYNTAX</span></span>

```
Set-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-DisableWAD] [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6d22-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6d22-105">DESCRIPTION</span></span>
<span data-ttu-id="f6d22-106">**Set-AzureRmVMAEMExtension** cmdlet 'i sanal makinenin yapılandırmasını güncelleştirerek sanal MAKINEDE yüklü SAP sistemlerini izlemeye yönelik desteği etkinleştirir veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f6d22-106">The **Set-AzureRmVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="f6d22-107">Cmdlet, performans verilerini toplayan ve SAP sistemi için bulunabilir kılan Azure Enhanced Monitoring (AEM) uzantısını yükler.</span><span class="sxs-lookup"><span data-stu-id="f6d22-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="f6d22-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6d22-108">EXAMPLES</span></span>

### <span data-ttu-id="f6d22-109">Örnek 1: AEM uzantısını kullanma</span><span class="sxs-lookup"><span data-stu-id="f6d22-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="f6d22-110">Bu komut, Contoso sunucusu adındaki sanal makineyi AEM uzantısını kullanacak şekilde yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="f6d22-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="f6d22-111">Komut, stddepolama adlı depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6d22-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="f6d22-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6d22-112">PARAMETERS</span></span>

### <span data-ttu-id="f6d22-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6d22-113">-DefaultProfile</span></span>
<span data-ttu-id="f6d22-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f6d22-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6d22-115">-DisableWAD</span><span class="sxs-lookup"><span data-stu-id="f6d22-115">-DisableWAD</span></span>
<span data-ttu-id="f6d22-116">Bu cmdlet 'in sanal makine için Azure tanılamalarını etkinleştirmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6d22-116">Indicates that this cmdlet does not enable Azure Diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="f6d22-117">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="f6d22-117">-EnableWAD</span></span>
<span data-ttu-id="f6d22-118">Bu parametre sağlanmışsa, commandme bu sanal makine için Windows Azure tanılamasını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="f6d22-118">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

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

### <span data-ttu-id="f6d22-119">-OSType</span><span class="sxs-lookup"><span data-stu-id="f6d22-119">-OSType</span></span>
<span data-ttu-id="f6d22-120">İşletim sistemi diskinin işletim sisteminin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6d22-120">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="f6d22-121">İşletim sistemi diskinin türü yoksa, bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f6d22-121">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="f6d22-122">Bu parametre için kabul edilebilir değerler: Windows ve Linux.</span><span class="sxs-lookup"><span data-stu-id="f6d22-122">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="f6d22-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6d22-123">-ResourceGroupName</span></span>
<span data-ttu-id="f6d22-124">Bu cmdlet 'in değiştirdiği sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6d22-124">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f6d22-125">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="f6d22-125">-SkipStorage</span></span>
<span data-ttu-id="f6d22-126">Bu cmdlet 'in depolama yapılandırmasını aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6d22-126">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="f6d22-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="f6d22-127">-VMName</span></span>
<span data-ttu-id="f6d22-128">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6d22-128">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f6d22-129">Bu cmdlet, bu parametrenin belirttiği sanal makine için AEM uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="f6d22-129">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="f6d22-130">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f6d22-130">-WADStorageAccountName</span></span>
<span data-ttu-id="f6d22-131">Bu cmdlet 'in LinuxDiagnostics veya IaaSDiagnostics uzantısını yapılandırmak için kullandığı depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6d22-131">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="f6d22-132">Sanal makine standart depolama hesabı kullanmazsa bu parametre için bir değer belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f6d22-132">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="f6d22-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6d22-133">CommonParameters</span></span>
<span data-ttu-id="f6d22-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6d22-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6d22-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6d22-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6d22-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6d22-136">INPUTS</span></span>

## <span data-ttu-id="f6d22-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6d22-137">OUTPUTS</span></span>

## <span data-ttu-id="f6d22-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6d22-138">NOTES</span></span>

## <span data-ttu-id="f6d22-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6d22-139">RELATED LINKS</span></span>

[<span data-ttu-id="f6d22-140">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f6d22-140">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="f6d22-141">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f6d22-141">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="f6d22-142">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f6d22-142">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


