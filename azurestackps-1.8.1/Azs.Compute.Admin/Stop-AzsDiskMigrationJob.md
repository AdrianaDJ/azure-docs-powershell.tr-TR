---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee1a9ae5a4d5ef7545ee9a3e071fcc06475034f4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934988"
---
# <span data-ttu-id="b9c9b-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="b9c9b-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="b9c9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9c9b-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c9b-103">Yönetilen disk geçiş işini iptal etme.</span><span class="sxs-lookup"><span data-stu-id="b9c9b-103">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="b9c9b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b9c9b-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob [[-Location] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="b9c9b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b9c9b-105">DESCRIPTION</span></span>
<span data-ttu-id="b9c9b-106">Disk geçiş işini iptal etme.</span><span class="sxs-lookup"><span data-stu-id="b9c9b-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="b9c9b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b9c9b-107">EXAMPLES</span></span>

### <span data-ttu-id="b9c9b-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b9c9b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsDiskMigrationJob -Location local -MigrationId $migration.MigrationId
```

<span data-ttu-id="b9c9b-109">Yönetilen disk geçiş işini iptal etme.</span><span class="sxs-lookup"><span data-stu-id="b9c9b-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="b9c9b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b9c9b-110">PARAMETERS</span></span>

### <span data-ttu-id="b9c9b-111">-Konum</span><span class="sxs-lookup"><span data-stu-id="b9c9b-111">-Location</span></span>
<span data-ttu-id="b9c9b-112">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="b9c9b-112">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c9b-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="b9c9b-113">-Name</span></span>
<span data-ttu-id="b9c9b-114">Geçiş işi GUID adı.</span><span class="sxs-lookup"><span data-stu-id="b9c9b-114">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MigrationId

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c9b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c9b-115">CommonParameters</span></span>
<span data-ttu-id="b9c9b-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b9c9b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c9b-117">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9c9b-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c9b-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b9c9b-118">INPUTS</span></span>

## <span data-ttu-id="b9c9b-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b9c9b-119">OUTPUTS</span></span>

### <span data-ttu-id="b9c9b-120">Microsoft. AzureStack. Management. COMPUTE. admin. modeller. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="b9c9b-120">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="b9c9b-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b9c9b-121">NOTES</span></span>

## <span data-ttu-id="b9c9b-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b9c9b-122">RELATED LINKS</span></span>

