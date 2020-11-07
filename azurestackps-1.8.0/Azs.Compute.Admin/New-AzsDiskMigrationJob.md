---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: db6eff0b0b0e0698c42dd7905cd3e5f7879345e1
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934666"
---
# <span data-ttu-id="4c341-101">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="4c341-101">New-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="4c341-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c341-102">SYNOPSIS</span></span>
<span data-ttu-id="4c341-103">Yönetilen diskleri belirtilen hedef paylaşıma geçirmek için yönetilen disk geçiş işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="4c341-103">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

## <span data-ttu-id="4c341-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c341-104">SYNTAX</span></span>

```
New-AzsDiskMigrationJob [-Disks] <Disk[]> [-TargetShare] <String> [[-Location] <String>] [-Name] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="4c341-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c341-105">DESCRIPTION</span></span>
<span data-ttu-id="4c341-106">Disk geçiş işi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4c341-106">Create a disk migration job.</span></span>

## <span data-ttu-id="4c341-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c341-107">EXAMPLES</span></span>

### <span data-ttu-id="4c341-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4c341-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsDiskMigrationJob -Name "MyMigrationJob" -Disks $disks -location local -TargetShare "\\SU1FileServer.azurestack.local\SU1_ObjStore"
```

<span data-ttu-id="4c341-109">İlk 20 disk için yönetilen disk geçiş işi başlatma</span><span class="sxs-lookup"><span data-stu-id="4c341-109">Start a managed disk migration job for the first 20 disks</span></span>

## <span data-ttu-id="4c341-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c341-110">PARAMETERS</span></span>

### <span data-ttu-id="4c341-111">-Diskler</span><span class="sxs-lookup"><span data-stu-id="4c341-111">-Disks</span></span>
<span data-ttu-id="4c341-112">Disk listesi parametreleri.</span><span class="sxs-lookup"><span data-stu-id="4c341-112">The parameters of disk list.</span></span>

```yaml
Type: Disk[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c341-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="4c341-113">-Location</span></span>
<span data-ttu-id="4c341-114">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="4c341-114">Location of the resource.</span></span>

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

### <span data-ttu-id="4c341-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="4c341-115">-Name</span></span>
<span data-ttu-id="4c341-116">Geçiş işi GUID adı.</span><span class="sxs-lookup"><span data-stu-id="4c341-116">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c341-117">-TargetShare</span><span class="sxs-lookup"><span data-stu-id="4c341-117">-TargetShare</span></span>
<span data-ttu-id="4c341-118">Hedef paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="4c341-118">The target share name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c341-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c341-119">CommonParameters</span></span>
<span data-ttu-id="4c341-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c341-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c341-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c341-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c341-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c341-122">INPUTS</span></span>

## <span data-ttu-id="4c341-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c341-123">OUTPUTS</span></span>

### <span data-ttu-id="4c341-124">Microsoft. AzureStack. Management. COMPUTE. admin. modeller. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="4c341-124">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="4c341-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c341-125">NOTES</span></span>

## <span data-ttu-id="4c341-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c341-126">RELATED LINKS</span></span>

