---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af9c5d2c5ebb547a6e09d2e4f4302ed2da470a39
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935023"
---
# <span data-ttu-id="99011-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="99011-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="99011-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99011-102">SYNOPSIS</span></span>
<span data-ttu-id="99011-103">Kapsayıcıyı belirtilen hedef paylaşıma geçirmek için kapsayıcı geçiş işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="99011-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="99011-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99011-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-ContainerName] <String>
 [-ShareName] <String> [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99011-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="99011-105">DESCRIPTION</span></span>
<span data-ttu-id="99011-106">Kapsayıcıyı belirtilen hedef paylaşıma geçirmek için kapsayıcı geçiş işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="99011-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="99011-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99011-107">EXAMPLES</span></span>

### <span data-ttu-id="99011-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="99011-108">EXAMPLE 1</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -ContainerName "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="99011-109">Kapsayıcı geçişi başlatır.</span><span class="sxs-lookup"><span data-stu-id="99011-109">Starts a container migration.</span></span>

## <span data-ttu-id="99011-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99011-110">PARAMETERS</span></span>

### <span data-ttu-id="99011-111">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="99011-111">-StorageAccountName</span></span>
<span data-ttu-id="99011-112">Kapsayıcının konumunu bulan depolama hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="99011-112">The name of storage account where the container locates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99011-113">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="99011-113">-ContainerName</span></span>
<span data-ttu-id="99011-114">Geçirilecek kapsayıcının adı.</span><span class="sxs-lookup"><span data-stu-id="99011-114">The name of the container to be migrated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99011-115">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="99011-115">-ShareName</span></span>
<span data-ttu-id="99011-116">Geçiş için belirtilen kapsayıcıyı içeren paylaşımın adı.</span><span class="sxs-lookup"><span data-stu-id="99011-116">Name of the share containing the container specified for migration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99011-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99011-117">-ResourceGroupName</span></span>
<span data-ttu-id="99011-118">Depolama kaynak sağlayıcısının altında kaydedildiği kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="99011-118">The resource group name in which the storage resource provider was registered under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99011-119">-FarmName</span><span class="sxs-lookup"><span data-stu-id="99011-119">-FarmName</span></span>
<span data-ttu-id="99011-120">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="99011-120">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99011-121">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="99011-121">-DestinationShareUncPath</span></span>
<span data-ttu-id="99011-122">Geçiş için hedef paylaşımın UNC yolu.</span><span class="sxs-lookup"><span data-stu-id="99011-122">The UNC path of the destination share for migration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99011-123">-Iş</span><span class="sxs-lookup"><span data-stu-id="99011-123">-AsJob</span></span>
<span data-ttu-id="99011-124">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="99011-124">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="99011-125">-Force</span><span class="sxs-lookup"><span data-stu-id="99011-125">-Force</span></span>
<span data-ttu-id="99011-126">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="99011-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="99011-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99011-127">-WhatIf</span></span>
<span data-ttu-id="99011-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="99011-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99011-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="99011-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99011-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="99011-130">-Confirm</span></span>
<span data-ttu-id="99011-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="99011-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99011-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99011-132">CommonParameters</span></span>
<span data-ttu-id="99011-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99011-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99011-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99011-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99011-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99011-135">INPUTS</span></span>

## <span data-ttu-id="99011-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99011-136">OUTPUTS</span></span>

## <span data-ttu-id="99011-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99011-137">NOTES</span></span>

## <span data-ttu-id="99011-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99011-138">RELATED LINKS</span></span>
