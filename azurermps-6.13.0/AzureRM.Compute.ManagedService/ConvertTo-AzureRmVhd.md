---
external help file: AzureRM.Compute.ManagedService-help.xml
Module Name: AzureRM.Compute.ManagedService
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute.managedservice/convertto-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
ms.openlocfilehash: 0fa0f2d5cb78fe96f05b818b5cbfdabca47cbdee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587271"
---
# <span data-ttu-id="29d96-101">ConvertTo-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="29d96-101">ConvertTo-AzureRmVhd</span></span>

## <span data-ttu-id="29d96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29d96-102">SYNOPSIS</span></span>
<span data-ttu-id="29d96-103">Hyper-V VM 'yi Azure destekli sanal sabit disk dosyalarına dönüştürme</span><span class="sxs-lookup"><span data-stu-id="29d96-103">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29d96-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="29d96-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVhd -HyperVVMName <String> -ExportPath <String> [-HyperVServer <String>] [-Force] [-AsJob]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29d96-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="29d96-105">DESCRIPTION</span></span>
<span data-ttu-id="29d96-106">Hyper-V VM 'yi Azure destekli sanal sabit disk dosyalarına dönüştürme</span><span class="sxs-lookup"><span data-stu-id="29d96-106">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

## <span data-ttu-id="29d96-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="29d96-107">EXAMPLES</span></span>

### <span data-ttu-id="29d96-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="29d96-108">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVhd -HyperVVMName 'test' -ExportPath '.';
.\test\Virtual Hard Disks\Converted\os.vhd
.\test\Virtual Hard Disks\Converted\disk.vhd
```

<span data-ttu-id="29d96-109">' Test ' adlı Hyper-V VM 'yi geçerli klasöre Azure desteklenen sanal sabit disk dosyalarına dönüştürün.</span><span class="sxs-lookup"><span data-stu-id="29d96-109">Convert Hyper-V VM named 'test' to Azure supported virtual hard disk files to the current folder.</span></span>

## <span data-ttu-id="29d96-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="29d96-110">PARAMETERS</span></span>

### <span data-ttu-id="29d96-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="29d96-111">-AsJob</span></span>
<span data-ttu-id="29d96-112">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="29d96-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="29d96-113">-ExportPath</span><span class="sxs-lookup"><span data-stu-id="29d96-113">-ExportPath</span></span>
<span data-ttu-id="29d96-114">Disk dosyalarını içerecek olan dışarı aktarma klasörü yolu.</span><span class="sxs-lookup"><span data-stu-id="29d96-114">The export folder path that will contain the disk files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29d96-115">-Force</span><span class="sxs-lookup"><span data-stu-id="29d96-115">-Force</span></span>
<span data-ttu-id="29d96-116">Var olan klasör bulunsa bile dışarı aktarmayı zorlayın.</span><span class="sxs-lookup"><span data-stu-id="29d96-116">Force the export even if existing folder is found.</span></span>

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

### <span data-ttu-id="29d96-117">-HyperVServer</span><span class="sxs-lookup"><span data-stu-id="29d96-117">-HyperVServer</span></span>
<span data-ttu-id="29d96-118">Varsayılan değer olarak ' localhost ' içeren Hyper-V sunucusu DNS adı.</span><span class="sxs-lookup"><span data-stu-id="29d96-118">The Hyper-V server DNS name, with 'localhost' as the default value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29d96-119">-Hiper Vvmname</span><span class="sxs-lookup"><span data-stu-id="29d96-119">-HyperVVMName</span></span>
<span data-ttu-id="29d96-120">Hyper-V adı adı.</span><span class="sxs-lookup"><span data-stu-id="29d96-120">The Hyper-V name name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29d96-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="29d96-121">-Confirm</span></span>
<span data-ttu-id="29d96-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="29d96-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29d96-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29d96-123">-WhatIf</span></span>
<span data-ttu-id="29d96-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="29d96-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29d96-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="29d96-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29d96-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29d96-126">CommonParameters</span></span>
<span data-ttu-id="29d96-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="29d96-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29d96-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29d96-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29d96-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="29d96-129">INPUTS</span></span>

### <span data-ttu-id="29d96-130">System. String</span><span class="sxs-lookup"><span data-stu-id="29d96-130">System.String</span></span>

## <span data-ttu-id="29d96-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="29d96-131">OUTPUTS</span></span>

### <span data-ttu-id="29d96-132">System. Management. Automation. PathInfo</span><span class="sxs-lookup"><span data-stu-id="29d96-132">System.Management.Automation.PathInfo</span></span>

## <span data-ttu-id="29d96-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="29d96-133">NOTES</span></span>

## <span data-ttu-id="29d96-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="29d96-134">RELATED LINKS</span></span>
