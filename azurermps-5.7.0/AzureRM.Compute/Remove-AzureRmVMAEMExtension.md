---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
ms.openlocfilehash: fb31bffbdb61c42ea1388c85b71f26af69056c54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589862"
---
# <span data-ttu-id="2e2de-101">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="2e2de-101">Remove-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="2e2de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e2de-102">SYNOPSIS</span></span>
<span data-ttu-id="2e2de-103">Sanal makineden AEM uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2e2de-103">Removes the AEM extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e2de-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e2de-104">SYNTAX</span></span>

```
Remove-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [<CommonParameters>]
```

## <span data-ttu-id="2e2de-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e2de-105">DESCRIPTION</span></span>
<span data-ttu-id="2e2de-106">**Remove-AzureRmVMAEMExtension** cmdlet 'i bir sanal makineden Azure Gelişmiş izleme (AEM) uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2e2de-106">The **Remove-AzureRmVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="2e2de-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e2de-107">EXAMPLES</span></span>

### <span data-ttu-id="2e2de-108">Örnek 1: AEM uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="2e2de-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="2e2de-109">Bu komut contoso-Server adlı sanal makinenin AEM uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2e2de-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="2e2de-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e2de-110">PARAMETERS</span></span>

### <span data-ttu-id="2e2de-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="2e2de-111">-Name</span></span>
<span data-ttu-id="2e2de-112">Bu cmdlet 'in AEM uzantısını kaldıran sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e2de-112">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e2de-113">-OSType</span><span class="sxs-lookup"><span data-stu-id="2e2de-113">-OSType</span></span>
<span data-ttu-id="2e2de-114">İşletim sistemi diskinin işletim sisteminin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e2de-114">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="2e2de-115">İşletim sistemi diskinin türü yoksa, bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2e2de-115">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="2e2de-116">Bu parametre için kabul edilebilir değerler: Windows ve Linux.</span><span class="sxs-lookup"><span data-stu-id="2e2de-116">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e2de-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e2de-117">-ResourceGroupName</span></span>
<span data-ttu-id="2e2de-118">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e2de-118">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="2e2de-119">Bu cmdlet, bu sanal makineden AEM uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2e2de-119">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="2e2de-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="2e2de-120">-VMName</span></span>
<span data-ttu-id="2e2de-121">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e2de-121">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="2e2de-122">Bu cmdlet, bu parametrenin belirttiği sanal makinenin AEM uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2e2de-122">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="2e2de-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e2de-123">CommonParameters</span></span>
<span data-ttu-id="2e2de-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e2de-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e2de-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e2de-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e2de-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e2de-126">INPUTS</span></span>

### <span data-ttu-id="2e2de-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2e2de-127">None</span></span>
<span data-ttu-id="2e2de-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="2e2de-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2e2de-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e2de-129">OUTPUTS</span></span>

## <span data-ttu-id="2e2de-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e2de-130">NOTES</span></span>

## <span data-ttu-id="2e2de-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e2de-131">RELATED LINKS</span></span>

[<span data-ttu-id="2e2de-132">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="2e2de-132">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="2e2de-133">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="2e2de-133">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="2e2de-134">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="2e2de-134">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


