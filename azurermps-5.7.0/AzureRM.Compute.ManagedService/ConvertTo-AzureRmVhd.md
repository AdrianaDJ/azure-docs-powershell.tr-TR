---
external help file: ''
Module Name: ''
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute.managedservice/convertto-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
ms.openlocfilehash: c440fa43a4e15abb5ab9f87d5b814fe3cbc55d63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588991"
---
# <span data-ttu-id="c1e1c-101">ConvertTo-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="c1e1c-101">ConvertTo-AzureRmVhd</span></span>

## <span data-ttu-id="c1e1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="c1e1c-103">Hyper-V VM 'yi Azure destekli sanal sabit disk dosyalarına dönüştürme</span><span class="sxs-lookup"><span data-stu-id="c1e1c-103">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1e1c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c1e1c-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVhd -HyperVVMName <String> -ExportPath <String> [-HyperVServer <String>] [-Force] [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="c1e1c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1e1c-105">DESCRIPTION</span></span>
<span data-ttu-id="c1e1c-106">Hyper-V VM 'yi Azure destekli sanal sabit disk dosyalarına dönüştürme</span><span class="sxs-lookup"><span data-stu-id="c1e1c-106">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

## <span data-ttu-id="c1e1c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c1e1c-107">EXAMPLES</span></span>

### <span data-ttu-id="c1e1c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c1e1c-108">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVhd -HyperVVMName 'test' -ExportPath '.';
.\test\Virtual Hard Disks\Converted\os.vhd
.\test\Virtual Hard Disks\Converted\disk.vhd
```

<span data-ttu-id="c1e1c-109">' Test ' adlı Hyper-V VM 'yi geçerli klasöre Azure desteklenen sanal sabit disk dosyalarına dönüştürün.</span><span class="sxs-lookup"><span data-stu-id="c1e1c-109">Convert Hyper-V VM named 'test' to Azure supported virtual hard disk files to the current folder.</span></span>

## <span data-ttu-id="c1e1c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c1e1c-110">PARAMETERS</span></span>

### <span data-ttu-id="c1e1c-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="c1e1c-111">-AsJob</span></span>
<span data-ttu-id="c1e1c-112">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="c1e1c-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e1c-113">-ExportPath</span><span class="sxs-lookup"><span data-stu-id="c1e1c-113">-ExportPath</span></span>
<span data-ttu-id="c1e1c-114">Disk dosyalarını içerecek olan dışarı aktarma klasörü yolu.</span><span class="sxs-lookup"><span data-stu-id="c1e1c-114">The export folder path that will contain the disk files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e1c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c1e1c-115">-Force</span></span>
<span data-ttu-id="c1e1c-116">Var olan klasör bulunsa bile dışarı aktarmayı zorlayın.</span><span class="sxs-lookup"><span data-stu-id="c1e1c-116">Force the export even if existing folder is found.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e1c-117">-HyperVServer</span><span class="sxs-lookup"><span data-stu-id="c1e1c-117">-HyperVServer</span></span>
<span data-ttu-id="c1e1c-118">Varsayılan değer olarak ' localhost ' içeren Hyper-V sunucusu DNS adı.</span><span class="sxs-lookup"><span data-stu-id="c1e1c-118">The Hyper-V server DNS name, with 'localhost' as the default value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e1c-119">-Hiper Vvmname</span><span class="sxs-lookup"><span data-stu-id="c1e1c-119">-HyperVVMName</span></span>
<span data-ttu-id="c1e1c-120">Hyper-V adı adı.</span><span class="sxs-lookup"><span data-stu-id="c1e1c-120">The Hyper-V name name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e1c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1e1c-121">CommonParameters</span></span>
<span data-ttu-id="c1e1c-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c1e1c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1e1c-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1e1c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1e1c-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c1e1c-124">INPUTS</span></span>

### <span data-ttu-id="c1e1c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c1e1c-125">System.String</span></span>

## <span data-ttu-id="c1e1c-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c1e1c-126">OUTPUTS</span></span>

### <span data-ttu-id="c1e1c-127">System. Management. Automation. PathInfo</span><span class="sxs-lookup"><span data-stu-id="c1e1c-127">System.Management.Automation.PathInfo</span></span>

## <span data-ttu-id="c1e1c-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c1e1c-128">NOTES</span></span>

## <span data-ttu-id="c1e1c-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c1e1c-129">RELATED LINKS</span></span>

