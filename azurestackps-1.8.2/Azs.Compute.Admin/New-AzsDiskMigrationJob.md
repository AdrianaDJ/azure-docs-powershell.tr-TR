---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: db6eff0b0b0e0698c42dd7905cd3e5f7879345e1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106788"
---
# <span data-ttu-id="7ce83-101">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="7ce83-101">New-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="7ce83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ce83-102">SYNOPSIS</span></span>
<span data-ttu-id="7ce83-103">Yönetilen diskleri belirtilen hedef paylaşıma geçirmek için yönetilen disk geçiş işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="7ce83-103">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

## <span data-ttu-id="7ce83-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7ce83-104">SYNTAX</span></span>

```
New-AzsDiskMigrationJob [-Disks] <Disk[]> [-TargetShare] <String> [[-Location] <String>] [-Name] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="7ce83-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ce83-105">DESCRIPTION</span></span>
<span data-ttu-id="7ce83-106">Disk geçiş işi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7ce83-106">Create a disk migration job.</span></span>

## <span data-ttu-id="7ce83-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7ce83-107">EXAMPLES</span></span>

### <span data-ttu-id="7ce83-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7ce83-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsDiskMigrationJob -Name "MyMigrationJob" -Disks $disks -location local -TargetShare "\\SU1FileServer.azurestack.local\SU1_ObjStore"
```

<span data-ttu-id="7ce83-109">İlk 20 disk için yönetilen disk geçiş işi başlatma</span><span class="sxs-lookup"><span data-stu-id="7ce83-109">Start a managed disk migration job for the first 20 disks</span></span>

## <span data-ttu-id="7ce83-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7ce83-110">PARAMETERS</span></span>

### <span data-ttu-id="7ce83-111">-Diskler</span><span class="sxs-lookup"><span data-stu-id="7ce83-111">-Disks</span></span>
<span data-ttu-id="7ce83-112">Disk listesi parametreleri.</span><span class="sxs-lookup"><span data-stu-id="7ce83-112">The parameters of disk list.</span></span>

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

### <span data-ttu-id="7ce83-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="7ce83-113">-Location</span></span>
<span data-ttu-id="7ce83-114">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="7ce83-114">Location of the resource.</span></span>

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

### <span data-ttu-id="7ce83-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="7ce83-115">-Name</span></span>
<span data-ttu-id="7ce83-116">Geçiş işi GUID adı.</span><span class="sxs-lookup"><span data-stu-id="7ce83-116">The migration job guid name.</span></span>

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

### <span data-ttu-id="7ce83-117">-TargetShare</span><span class="sxs-lookup"><span data-stu-id="7ce83-117">-TargetShare</span></span>
<span data-ttu-id="7ce83-118">Hedef paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="7ce83-118">The target share name.</span></span>

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

### <span data-ttu-id="7ce83-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ce83-119">CommonParameters</span></span>
<span data-ttu-id="7ce83-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7ce83-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ce83-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ce83-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ce83-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7ce83-122">INPUTS</span></span>

## <span data-ttu-id="7ce83-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7ce83-123">OUTPUTS</span></span>

### <span data-ttu-id="7ce83-124">Microsoft. AzureStack. Management. COMPUTE. admin. modeller. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="7ce83-124">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="7ce83-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7ce83-125">NOTES</span></span>

## <span data-ttu-id="7ce83-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7ce83-126">RELATED LINKS</span></span>

