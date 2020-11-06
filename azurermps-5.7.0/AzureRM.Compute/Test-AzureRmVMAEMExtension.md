---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
ms.openlocfilehash: d766102b0e87968e59bdd9bf63157dd62e977a25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586773"
---
# <span data-ttu-id="355de-101">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="355de-101">Test-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="355de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="355de-102">SYNOPSIS</span></span>
<span data-ttu-id="355de-103">AEM uzantısının yapılandırmasını denetler.</span><span class="sxs-lookup"><span data-stu-id="355de-103">Checks the configuration of the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="355de-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="355de-104">SYNTAX</span></span>

```
Test-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [<CommonParameters>]
```

## <span data-ttu-id="355de-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="355de-105">DESCRIPTION</span></span>
<span data-ttu-id="355de-106">**Test-AzureRmVMAEMExtension** cmdlet 'ı, Azure Gelişmiş izleme (AEM) uzantısının yapılandırmasını denetler.</span><span class="sxs-lookup"><span data-stu-id="355de-106">The **Test-AzureRmVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="355de-107">AEM uzantısı performans verilerini toplar.</span><span class="sxs-lookup"><span data-stu-id="355de-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="355de-108">Bu cmdlet performans verilerinin kullanılabilir olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="355de-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="355de-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="355de-109">EXAMPLES</span></span>

### <span data-ttu-id="355de-110">Örnek 1: AEM uzantısının yapılandırmasını denetleme</span><span class="sxs-lookup"><span data-stu-id="355de-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="355de-111">Bu komut, Contoso sunucusu adlı sanal makinenin AEM uzantısının yapılandırmasını denetler.</span><span class="sxs-lookup"><span data-stu-id="355de-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="355de-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="355de-112">PARAMETERS</span></span>

### <span data-ttu-id="355de-113">-OSType</span><span class="sxs-lookup"><span data-stu-id="355de-113">-OSType</span></span>
<span data-ttu-id="355de-114">İşletim sistemi diskinin işletim sisteminin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="355de-114">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="355de-115">İşletim sistemi diskinin türü yoksa, bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="355de-115">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="355de-116">Bu parametre için kabul edilebilir değerler: Windows ve Linux.</span><span class="sxs-lookup"><span data-stu-id="355de-116">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="355de-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="355de-117">-ResourceGroupName</span></span>
<span data-ttu-id="355de-118">Bu cmdlet 'in denetlediği sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="355de-118">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="355de-119">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="355de-119">-SkipStorageCheck</span></span>
<span data-ttu-id="355de-120">Bu cmdlet 'in depolama yapılandırmasını gözden aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="355de-120">Indicates that this cmdlet skips the check of storage configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="355de-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="355de-121">-VMName</span></span>
<span data-ttu-id="355de-122">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="355de-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="355de-123">Bu cmdlet, bu parametrenin belirttiği sanal makinenin AEM uzantısını sınar.</span><span class="sxs-lookup"><span data-stu-id="355de-123">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="355de-124">-Waittimeınminutes</span><span class="sxs-lookup"><span data-stu-id="355de-124">-WaitTimeInMinutes</span></span>
<span data-ttu-id="355de-125">Depolama yapılandırması denetimi için zaman aşımı süresini dakika olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="355de-125">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="355de-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="355de-126">CommonParameters</span></span>
<span data-ttu-id="355de-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="355de-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="355de-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="355de-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="355de-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="355de-129">INPUTS</span></span>

### <span data-ttu-id="355de-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="355de-130">None</span></span>
<span data-ttu-id="355de-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="355de-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="355de-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="355de-132">OUTPUTS</span></span>

## <span data-ttu-id="355de-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="355de-133">NOTES</span></span>

## <span data-ttu-id="355de-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="355de-134">RELATED LINKS</span></span>

[<span data-ttu-id="355de-135">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="355de-135">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="355de-136">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="355de-136">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="355de-137">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="355de-137">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)


