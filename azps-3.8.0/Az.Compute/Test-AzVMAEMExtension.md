---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/test-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
ms.openlocfilehash: ffc22a8937e56537de167046f661ee4b5d262fed
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104593"
---
# <span data-ttu-id="0595e-101">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0595e-101">Test-AzVMAEMExtension</span></span>

## <span data-ttu-id="0595e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0595e-102">SYNOPSIS</span></span>
<span data-ttu-id="0595e-103">AEM uzantısının yapılandırmasını denetler.</span><span class="sxs-lookup"><span data-stu-id="0595e-103">Checks the configuration of the AEM extension.</span></span>

## <span data-ttu-id="0595e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0595e-104">SYNTAX</span></span>

```
Test-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0595e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0595e-105">DESCRIPTION</span></span>
<span data-ttu-id="0595e-106">**Test-AzVMAEMExtension** cmdlet 'ı, Azure Gelişmiş izleme (AEM) uzantısının yapılandırmasını denetler.</span><span class="sxs-lookup"><span data-stu-id="0595e-106">The **Test-AzVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="0595e-107">AEM uzantısı performans verilerini toplar.</span><span class="sxs-lookup"><span data-stu-id="0595e-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="0595e-108">Bu cmdlet performans verilerinin kullanılabilir olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="0595e-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="0595e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0595e-109">EXAMPLES</span></span>

### <span data-ttu-id="0595e-110">Örnek 1: AEM uzantısının yapılandırmasını denetleme</span><span class="sxs-lookup"><span data-stu-id="0595e-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="0595e-111">Bu komut, Contoso sunucusu adlı sanal makinenin AEM uzantısının yapılandırmasını denetler.</span><span class="sxs-lookup"><span data-stu-id="0595e-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="0595e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0595e-112">PARAMETERS</span></span>

### <span data-ttu-id="0595e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0595e-113">-DefaultProfile</span></span>
<span data-ttu-id="0595e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0595e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0595e-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="0595e-115">-OSType</span></span>
<span data-ttu-id="0595e-116">İşletim sistemi diskinin işletim sisteminin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0595e-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="0595e-117">İşletim sistemi diskinin türü yoksa, bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="0595e-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="0595e-118">Bu parametre için kabul edilebilir değerler: Windows ve Linux.</span><span class="sxs-lookup"><span data-stu-id="0595e-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="0595e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0595e-119">-ResourceGroupName</span></span>
<span data-ttu-id="0595e-120">Bu cmdlet 'in denetlediği sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0595e-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="0595e-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="0595e-121">-SkipStorageCheck</span></span>
<span data-ttu-id="0595e-122">Bu cmdlet 'in depolama yapılandırmasını gözden aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0595e-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

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

### <span data-ttu-id="0595e-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="0595e-123">-VMName</span></span>
<span data-ttu-id="0595e-124">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0595e-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="0595e-125">Bu cmdlet, bu parametrenin belirttiği sanal makinenin AEM uzantısını sınar.</span><span class="sxs-lookup"><span data-stu-id="0595e-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="0595e-126">-Waittimeınminutes</span><span class="sxs-lookup"><span data-stu-id="0595e-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="0595e-127">Depolama yapılandırması denetimi için zaman aşımı süresini dakika olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="0595e-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0595e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0595e-128">CommonParameters</span></span>
<span data-ttu-id="0595e-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0595e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0595e-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0595e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0595e-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0595e-131">INPUTS</span></span>

### <span data-ttu-id="0595e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0595e-132">System.String</span></span>

## <span data-ttu-id="0595e-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0595e-133">OUTPUTS</span></span>

### <span data-ttu-id="0595e-134">Microsoft. Azure. Commands. COMPUTE. Extension. AEM. AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="0595e-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="0595e-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0595e-135">NOTES</span></span>

## <span data-ttu-id="0595e-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0595e-136">RELATED LINKS</span></span>

[<span data-ttu-id="0595e-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0595e-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="0595e-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0595e-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="0595e-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0595e-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)


