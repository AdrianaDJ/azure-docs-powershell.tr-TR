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
ms.locfileid: "93934289"
---
# <span data-ttu-id="64673-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="64673-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="64673-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64673-102">SYNOPSIS</span></span>
<span data-ttu-id="64673-103">Kapsayıcıyı belirtilen hedef paylaşıma geçirmek için kapsayıcı geçiş işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="64673-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="64673-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="64673-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-Name] <String> [-ShareName] <String>
 [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64673-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="64673-105">DESCRIPTION</span></span>
<span data-ttu-id="64673-106">Kapsayıcıyı belirtilen hedef paylaşıma geçirmek için kapsayıcı geçiş işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="64673-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="64673-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="64673-107">EXAMPLES</span></span>

### <span data-ttu-id="64673-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="64673-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -Name "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="64673-109">Kapsayıcı geçişi başlatır.</span><span class="sxs-lookup"><span data-stu-id="64673-109">Starts a container migration.</span></span>

## <span data-ttu-id="64673-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="64673-110">PARAMETERS</span></span>

### <span data-ttu-id="64673-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="64673-111">-AsJob</span></span>
<span data-ttu-id="64673-112">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="64673-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="64673-113">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="64673-113">-DestinationShareUncPath</span></span>
<span data-ttu-id="64673-114">Geçiş için hedef paylaşımın UNC yolu.</span><span class="sxs-lookup"><span data-stu-id="64673-114">The UNC path of the destination share for migration.</span></span>

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

### <span data-ttu-id="64673-115">-FarmName</span><span class="sxs-lookup"><span data-stu-id="64673-115">-FarmName</span></span>
<span data-ttu-id="64673-116">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="64673-116">Farm Id.</span></span>

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

### <span data-ttu-id="64673-117">-Force</span><span class="sxs-lookup"><span data-stu-id="64673-117">-Force</span></span>
<span data-ttu-id="64673-118">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="64673-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="64673-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="64673-119">-Name</span></span>
<span data-ttu-id="64673-120">Geçirilecek kapsayıcının adı.</span><span class="sxs-lookup"><span data-stu-id="64673-120">The name of the container to be migrated.</span></span>

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

### <span data-ttu-id="64673-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64673-121">-ResourceGroupName</span></span>
<span data-ttu-id="64673-122">Depolama kaynak sağlayıcısının altında kaydedildiği kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="64673-122">The resource group name in which the storage resource provider was registered under.</span></span>

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

### <span data-ttu-id="64673-123">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="64673-123">-ShareName</span></span>
<span data-ttu-id="64673-124">Geçiş için belirtilen kapsayıcıyı içeren paylaşımın adı.</span><span class="sxs-lookup"><span data-stu-id="64673-124">Name of the share containing the container specified for migration.</span></span>

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

### <span data-ttu-id="64673-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="64673-125">-StorageAccountName</span></span>
<span data-ttu-id="64673-126">Kapsayıcının konumunu bulan depolama hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="64673-126">The name of storage account where the container locates.</span></span>

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

### <span data-ttu-id="64673-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="64673-127">-Confirm</span></span>
<span data-ttu-id="64673-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="64673-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64673-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64673-129">-WhatIf</span></span>
<span data-ttu-id="64673-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="64673-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64673-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="64673-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64673-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64673-132">CommonParameters</span></span>
<span data-ttu-id="64673-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="64673-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64673-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64673-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64673-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="64673-135">INPUTS</span></span>

## <span data-ttu-id="64673-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="64673-136">OUTPUTS</span></span>

## <span data-ttu-id="64673-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="64673-137">NOTES</span></span>

## <span data-ttu-id="64673-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="64673-138">RELATED LINKS</span></span>

