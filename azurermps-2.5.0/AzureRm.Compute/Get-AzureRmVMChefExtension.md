---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmchefextension
schema: 2.0.0
ms.openlocfilehash: e9047b681e669975e7113eb3970b2ee6573a68d5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939169"
---
# <span data-ttu-id="f2332-101">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f2332-101">Get-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="f2332-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2332-102">SYNOPSIS</span></span>
<span data-ttu-id="f2332-103">Bir Çef uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="f2332-103">Gets information about a Chef extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2332-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2332-104">SYNTAX</span></span>

### <span data-ttu-id="f2332-105">UX</span><span class="sxs-lookup"><span data-stu-id="f2332-105">Linux</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Linux] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2332-106">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="f2332-106">Windows</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Windows] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2332-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2332-107">DESCRIPTION</span></span>
<span data-ttu-id="f2332-108">**Get-AzureVMChefExtension** cmdlet 'i sanal makinede yüklü bir Chef uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="f2332-108">The **Get-AzureVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="f2332-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2332-109">EXAMPLES</span></span>

### <span data-ttu-id="f2332-110">Örnek 1: Windows sanal makinesi için Chef uzantısının ayrıntılarını alma-</span><span class="sxs-lookup"><span data-stu-id="f2332-110">Example 1: Get the details of Chef extension for a Windows virtual machine-</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="f2332-111">Bu komut, ResourceGroup001 adındaki kaynak grubuna ait olan WindowsVM001 adındaki bir Windows sanal makinesinden Chef uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="f2332-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="f2332-112">Örnek 2: Linux sanal makinesi için Chef uzantısının ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="f2332-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="f2332-113">Bu komut, LinuxVM001 adındaki bir Linux sanal makinesinden ResourceGroup002 adındaki kaynak grubuna ait Chef uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="f2332-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="f2332-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2332-114">PARAMETERS</span></span>

### <span data-ttu-id="f2332-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2332-115">-DefaultProfile</span></span>
<span data-ttu-id="f2332-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f2332-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2332-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="f2332-117">-Linux</span></span>
<span data-ttu-id="f2332-118">Bu cmdlet 'in Linux sanal makinede çalıştığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f2332-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2332-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="f2332-119">-Name</span></span>
<span data-ttu-id="f2332-120">Chef uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2332-120">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="f2332-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2332-121">-ResourceGroupName</span></span>
<span data-ttu-id="f2332-122">Sanal makineyi içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2332-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="f2332-123">-Durum</span><span class="sxs-lookup"><span data-stu-id="f2332-123">-Status</span></span>
<span data-ttu-id="f2332-124">Bu cmdlet 'in yalnızca Chef uzantısının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f2332-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2332-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="f2332-125">-VMName</span></span>
<span data-ttu-id="f2332-126">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2332-126">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="f2332-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="f2332-127">-Windows</span></span>
<span data-ttu-id="f2332-128">Bu cmdlet 'in bir Windows sanal makinesi için olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="f2332-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2332-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2332-129">CommonParameters</span></span>
<span data-ttu-id="f2332-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2332-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2332-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2332-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2332-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2332-132">INPUTS</span></span>

### <span data-ttu-id="f2332-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f2332-133">None</span></span>
<span data-ttu-id="f2332-134">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="f2332-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f2332-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2332-135">OUTPUTS</span></span>

### <span data-ttu-id="f2332-136">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="f2332-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="f2332-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2332-137">NOTES</span></span>

## <span data-ttu-id="f2332-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2332-138">RELATED LINKS</span></span>

[<span data-ttu-id="f2332-139">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f2332-139">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)

[<span data-ttu-id="f2332-140">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f2332-140">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)


