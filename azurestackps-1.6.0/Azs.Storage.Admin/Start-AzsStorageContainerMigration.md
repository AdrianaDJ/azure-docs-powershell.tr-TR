---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54016a200b4304c7e37777202a8450fc9ad10e1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751305"
---
# <span data-ttu-id="657fb-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="657fb-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="657fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="657fb-102">SYNOPSIS</span></span>
<span data-ttu-id="657fb-103">Kapsayıcıyı belirtilen hedef paylaşıma geçirmek için kapsayıcı geçiş işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="657fb-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="657fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="657fb-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-Name] <String> [-ShareName] <String>
 [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="657fb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="657fb-105">DESCRIPTION</span></span>
<span data-ttu-id="657fb-106">Kapsayıcıyı belirtilen hedef paylaşıma geçirmek için kapsayıcı geçiş işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="657fb-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="657fb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="657fb-107">EXAMPLES</span></span>

### <span data-ttu-id="657fb-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="657fb-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -Name "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="657fb-109">Kapsayıcı geçişi başlatır.</span><span class="sxs-lookup"><span data-stu-id="657fb-109">Starts a container migration.</span></span>

## <span data-ttu-id="657fb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="657fb-110">PARAMETERS</span></span>

### <span data-ttu-id="657fb-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="657fb-111">-AsJob</span></span>
<span data-ttu-id="657fb-112">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="657fb-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="657fb-113">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="657fb-113">-DestinationShareUncPath</span></span>
<span data-ttu-id="657fb-114">Geçiş için hedef paylaşımın UNC yolu.</span><span class="sxs-lookup"><span data-stu-id="657fb-114">The UNC path of the destination share for migration.</span></span>

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

### <span data-ttu-id="657fb-115">-FarmName</span><span class="sxs-lookup"><span data-stu-id="657fb-115">-FarmName</span></span>
<span data-ttu-id="657fb-116">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="657fb-116">Farm Id.</span></span>

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

### <span data-ttu-id="657fb-117">-Force</span><span class="sxs-lookup"><span data-stu-id="657fb-117">-Force</span></span>
<span data-ttu-id="657fb-118">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="657fb-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="657fb-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="657fb-119">-Name</span></span>
<span data-ttu-id="657fb-120">Geçirilecek kapsayıcının adı.</span><span class="sxs-lookup"><span data-stu-id="657fb-120">The name of the container to be migrated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="657fb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="657fb-121">-ResourceGroupName</span></span>
<span data-ttu-id="657fb-122">Depolama kaynak sağlayıcısının altında kaydedildiği kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="657fb-122">The resource group name in which the storage resource provider was registered under.</span></span>

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

### <span data-ttu-id="657fb-123">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="657fb-123">-ShareName</span></span>
<span data-ttu-id="657fb-124">Geçiş için belirtilen kapsayıcıyı içeren paylaşımın adı.</span><span class="sxs-lookup"><span data-stu-id="657fb-124">Name of the share containing the container specified for migration.</span></span>

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

### <span data-ttu-id="657fb-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="657fb-125">-StorageAccountName</span></span>
<span data-ttu-id="657fb-126">Kapsayıcının konumunu bulan depolama hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="657fb-126">The name of storage account where the container locates.</span></span>

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

### <span data-ttu-id="657fb-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="657fb-127">-Confirm</span></span>
<span data-ttu-id="657fb-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="657fb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="657fb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="657fb-129">-WhatIf</span></span>
<span data-ttu-id="657fb-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="657fb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="657fb-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="657fb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="657fb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="657fb-132">CommonParameters</span></span>
<span data-ttu-id="657fb-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="657fb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="657fb-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="657fb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="657fb-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="657fb-135">INPUTS</span></span>

## <span data-ttu-id="657fb-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="657fb-136">OUTPUTS</span></span>

## <span data-ttu-id="657fb-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="657fb-137">NOTES</span></span>

## <span data-ttu-id="657fb-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="657fb-138">RELATED LINKS</span></span>

