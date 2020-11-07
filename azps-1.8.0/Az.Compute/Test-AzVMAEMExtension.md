---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/test-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
ms.openlocfilehash: c5c799d9bd9ea75f6540a84090644200c537f5d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761207"
---
# <span data-ttu-id="8736c-101">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="8736c-101">Test-AzVMAEMExtension</span></span>

## <span data-ttu-id="8736c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8736c-102">SYNOPSIS</span></span>
<span data-ttu-id="8736c-103">AEM uzantısının yapılandırmasını denetler.</span><span class="sxs-lookup"><span data-stu-id="8736c-103">Checks the configuration of the AEM extension.</span></span>

## <span data-ttu-id="8736c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8736c-104">SYNTAX</span></span>

```
Test-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8736c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8736c-105">DESCRIPTION</span></span>
<span data-ttu-id="8736c-106">**Test-AzVMAEMExtension** cmdlet 'ı, Azure Gelişmiş izleme (AEM) uzantısının yapılandırmasını denetler.</span><span class="sxs-lookup"><span data-stu-id="8736c-106">The **Test-AzVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="8736c-107">AEM uzantısı performans verilerini toplar.</span><span class="sxs-lookup"><span data-stu-id="8736c-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="8736c-108">Bu cmdlet performans verilerinin kullanılabilir olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="8736c-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="8736c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8736c-109">EXAMPLES</span></span>

### <span data-ttu-id="8736c-110">Örnek 1: AEM uzantısının yapılandırmasını denetleme</span><span class="sxs-lookup"><span data-stu-id="8736c-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="8736c-111">Bu komut, Contoso sunucusu adlı sanal makinenin AEM uzantısının yapılandırmasını denetler.</span><span class="sxs-lookup"><span data-stu-id="8736c-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="8736c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8736c-112">PARAMETERS</span></span>

### <span data-ttu-id="8736c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8736c-113">-DefaultProfile</span></span>
<span data-ttu-id="8736c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8736c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8736c-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="8736c-115">-OSType</span></span>
<span data-ttu-id="8736c-116">İşletim sistemi diskinin işletim sisteminin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8736c-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="8736c-117">İşletim sistemi diskinin türü yoksa, bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8736c-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="8736c-118">Bu parametre için kabul edilebilir değerler: Windows ve Linux.</span><span class="sxs-lookup"><span data-stu-id="8736c-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="8736c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8736c-119">-ResourceGroupName</span></span>
<span data-ttu-id="8736c-120">Bu cmdlet 'in denetlediği sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8736c-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="8736c-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="8736c-121">-SkipStorageCheck</span></span>
<span data-ttu-id="8736c-122">Bu cmdlet 'in depolama yapılandırmasını gözden aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8736c-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

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

### <span data-ttu-id="8736c-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="8736c-123">-VMName</span></span>
<span data-ttu-id="8736c-124">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8736c-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="8736c-125">Bu cmdlet, bu parametrenin belirttiği sanal makinenin AEM uzantısını sınar.</span><span class="sxs-lookup"><span data-stu-id="8736c-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="8736c-126">-Waittimeınminutes</span><span class="sxs-lookup"><span data-stu-id="8736c-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="8736c-127">Depolama yapılandırması denetimi için zaman aşımı süresini dakika olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="8736c-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

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

### <span data-ttu-id="8736c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8736c-128">CommonParameters</span></span>
<span data-ttu-id="8736c-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8736c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8736c-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8736c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8736c-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8736c-131">INPUTS</span></span>

### <span data-ttu-id="8736c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8736c-132">System.String</span></span>

## <span data-ttu-id="8736c-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8736c-133">OUTPUTS</span></span>

### <span data-ttu-id="8736c-134">Microsoft. Azure. Commands. COMPUTE. Extension. AEM. AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="8736c-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="8736c-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8736c-135">NOTES</span></span>

## <span data-ttu-id="8736c-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8736c-136">RELATED LINKS</span></span>

[<span data-ttu-id="8736c-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="8736c-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="8736c-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="8736c-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="8736c-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="8736c-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)


