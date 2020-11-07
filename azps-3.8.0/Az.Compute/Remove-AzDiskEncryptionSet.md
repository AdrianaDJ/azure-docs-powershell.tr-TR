---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: a15dd51bad097aafcc517fbef67f89d65b076380
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938548"
---
# <span data-ttu-id="7267d-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7267d-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="7267d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7267d-102">SYNOPSIS</span></span>
<span data-ttu-id="7267d-103">Disk şifrelemesi kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7267d-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="7267d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7267d-104">SYNTAX</span></span>

### <span data-ttu-id="7267d-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7267d-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7267d-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="7267d-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7267d-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="7267d-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7267d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7267d-108">DESCRIPTION</span></span>
<span data-ttu-id="7267d-109">Disk şifrelemesi kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7267d-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="7267d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7267d-110">EXAMPLES</span></span>

### <span data-ttu-id="7267d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7267d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="7267d-112">' RG1 ' içindeki ' enc1 ' disk şifrelemesi kümesini silme</span><span class="sxs-lookup"><span data-stu-id="7267d-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="7267d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7267d-113">PARAMETERS</span></span>

### <span data-ttu-id="7267d-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="7267d-114">-AsJob</span></span>
<span data-ttu-id="7267d-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7267d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7267d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7267d-116">-DefaultProfile</span></span>
<span data-ttu-id="7267d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7267d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7267d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7267d-118">-Force</span></span>
<span data-ttu-id="7267d-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="7267d-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7267d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7267d-120">-InputObject</span></span>
<span data-ttu-id="7267d-121">Disk şifrelemesi kümesinin yerel nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7267d-121">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7267d-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="7267d-122">-Name</span></span>
<span data-ttu-id="7267d-123">Disk şifreleme kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="7267d-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7267d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7267d-124">-ResourceGroupName</span></span>
<span data-ttu-id="7267d-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7267d-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7267d-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7267d-126">-ResourceId</span></span>
<span data-ttu-id="7267d-127">Kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7267d-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7267d-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="7267d-128">-Confirm</span></span>
<span data-ttu-id="7267d-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7267d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7267d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7267d-130">-WhatIf</span></span>
<span data-ttu-id="7267d-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7267d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7267d-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7267d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7267d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7267d-133">CommonParameters</span></span>
<span data-ttu-id="7267d-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7267d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7267d-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7267d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7267d-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7267d-136">INPUTS</span></span>

### <span data-ttu-id="7267d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7267d-137">System.String</span></span>

### <span data-ttu-id="7267d-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDıskencryptionset</span><span class="sxs-lookup"><span data-stu-id="7267d-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="7267d-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7267d-139">OUTPUTS</span></span>

### <span data-ttu-id="7267d-140">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="7267d-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="7267d-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7267d-141">NOTES</span></span>

## <span data-ttu-id="7267d-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7267d-142">RELATED LINKS</span></span>
