---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee1a9ae5a4d5ef7545ee9a3e071fcc06475034f4
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934654"
---
# <span data-ttu-id="c4cd0-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="c4cd0-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="c4cd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4cd0-102">SYNOPSIS</span></span>
<span data-ttu-id="c4cd0-103">Yönetilen disk geçiş işini iptal etme.</span><span class="sxs-lookup"><span data-stu-id="c4cd0-103">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="c4cd0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c4cd0-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob [[-Location] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="c4cd0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4cd0-105">DESCRIPTION</span></span>
<span data-ttu-id="c4cd0-106">Disk geçiş işini iptal etme.</span><span class="sxs-lookup"><span data-stu-id="c4cd0-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="c4cd0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c4cd0-107">EXAMPLES</span></span>

### <span data-ttu-id="c4cd0-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c4cd0-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsDiskMigrationJob -Location local -MigrationId $migration.MigrationId
```

<span data-ttu-id="c4cd0-109">Yönetilen disk geçiş işini iptal etme.</span><span class="sxs-lookup"><span data-stu-id="c4cd0-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="c4cd0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c4cd0-110">PARAMETERS</span></span>

### <span data-ttu-id="c4cd0-111">-Konum</span><span class="sxs-lookup"><span data-stu-id="c4cd0-111">-Location</span></span>
<span data-ttu-id="c4cd0-112">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="c4cd0-112">Location of the resource.</span></span>

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

### <span data-ttu-id="c4cd0-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="c4cd0-113">-Name</span></span>
<span data-ttu-id="c4cd0-114">Geçiş işi GUID adı.</span><span class="sxs-lookup"><span data-stu-id="c4cd0-114">The migration job guid name.</span></span>

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

### <span data-ttu-id="c4cd0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4cd0-115">CommonParameters</span></span>
<span data-ttu-id="c4cd0-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c4cd0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4cd0-117">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4cd0-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4cd0-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c4cd0-118">INPUTS</span></span>

## <span data-ttu-id="c4cd0-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c4cd0-119">OUTPUTS</span></span>

### <span data-ttu-id="c4cd0-120">Microsoft. AzureStack. Management. COMPUTE. admin. modeller. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="c4cd0-120">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="c4cd0-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c4cd0-121">NOTES</span></span>

## <span data-ttu-id="c4cd0-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c4cd0-122">RELATED LINKS</span></span>

