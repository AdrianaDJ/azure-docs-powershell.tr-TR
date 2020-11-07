---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 224d11aba6eece63c7c080415253b4833c665cee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936931"
---
# <span data-ttu-id="1d93c-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1d93c-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="1d93c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d93c-102">SYNOPSIS</span></span>
<span data-ttu-id="1d93c-103">Sanal makineden AEM uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1d93c-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="1d93c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1d93c-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d93c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d93c-105">DESCRIPTION</span></span>
<span data-ttu-id="1d93c-106">**Remove-AzVMAEMExtension** cmdlet 'i bir sanal makineden Azure Gelişmiş izleme (AEM) uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1d93c-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="1d93c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1d93c-107">EXAMPLES</span></span>

### <span data-ttu-id="1d93c-108">Örnek 1: AEM uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="1d93c-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="1d93c-109">Bu komut contoso-Server adlı sanal makinenin AEM uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1d93c-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="1d93c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1d93c-110">PARAMETERS</span></span>

### <span data-ttu-id="1d93c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d93c-111">-DefaultProfile</span></span>
<span data-ttu-id="1d93c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1d93c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d93c-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="1d93c-113">-Name</span></span>
<span data-ttu-id="1d93c-114">Bu cmdlet 'in AEM uzantısını kaldıran sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d93c-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="1d93c-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="1d93c-115">-OSType</span></span>
<span data-ttu-id="1d93c-116">İşletim sistemi diskinin işletim sisteminin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d93c-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="1d93c-117">İşletim sistemi diskinin türü yoksa, bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1d93c-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="1d93c-118">Bu parametre için kabul edilebilir değerler: Windows ve Linux.</span><span class="sxs-lookup"><span data-stu-id="1d93c-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="1d93c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d93c-119">-ResourceGroupName</span></span>
<span data-ttu-id="1d93c-120">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d93c-120">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="1d93c-121">Bu cmdlet, bu sanal makineden AEM uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1d93c-121">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="1d93c-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="1d93c-122">-VMName</span></span>
<span data-ttu-id="1d93c-123">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d93c-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="1d93c-124">Bu cmdlet, bu parametrenin belirttiği sanal makinenin AEM uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1d93c-124">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="1d93c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d93c-125">CommonParameters</span></span>
<span data-ttu-id="1d93c-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1d93c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d93c-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d93c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d93c-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1d93c-128">INPUTS</span></span>

### <span data-ttu-id="1d93c-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1d93c-129">None</span></span>
<span data-ttu-id="1d93c-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="1d93c-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1d93c-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1d93c-131">OUTPUTS</span></span>

### <span data-ttu-id="1d93c-132">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1d93c-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1d93c-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1d93c-133">NOTES</span></span>

## <span data-ttu-id="1d93c-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1d93c-134">RELATED LINKS</span></span>

[<span data-ttu-id="1d93c-135">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1d93c-135">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="1d93c-136">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1d93c-136">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="1d93c-137">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1d93c-137">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


