---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0207d9d2353954fc1997f5752ac6dad26dbdfa13
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934836"
---
# <span data-ttu-id="ea286-101">Get-AzsStorageContainerMigrationStatus</span><span class="sxs-lookup"><span data-stu-id="ea286-101">Get-AzsStorageContainerMigrationStatus</span></span>

## <span data-ttu-id="ea286-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea286-102">SYNOPSIS</span></span>
<span data-ttu-id="ea286-103">Kapsayıcı geçiş işinin durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="ea286-103">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="ea286-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea286-104">SYNTAX</span></span>

```
Get-AzsStorageContainerMigrationStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea286-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea286-105">DESCRIPTION</span></span>
<span data-ttu-id="ea286-106">Kapsayıcı geçiş işinin durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="ea286-106">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="ea286-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea286-107">EXAMPLES</span></span>

### <span data-ttu-id="ea286-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ea286-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageContainerMigrationStatus -FarmName "6ed442a3-ec47-4145-b2f0-9b90377b01d0" -JobId "6478ef3b-b7d5-4827-8d47-551c6afb9dd4"
```

<span data-ttu-id="ea286-109">Kapsayıcı geçiş işinin durumunu edinin.</span><span class="sxs-lookup"><span data-stu-id="ea286-109">Get the status of a container migration job.</span></span>

## <span data-ttu-id="ea286-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea286-110">PARAMETERS</span></span>

### <span data-ttu-id="ea286-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="ea286-111">-FarmName</span></span>
<span data-ttu-id="ea286-112">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="ea286-112">Farm Id.</span></span>

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

### <span data-ttu-id="ea286-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="ea286-113">-JobId</span></span>
<span data-ttu-id="ea286-114">İşlem kimliği.</span><span class="sxs-lookup"><span data-stu-id="ea286-114">Operation Id.</span></span>

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

### <span data-ttu-id="ea286-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea286-115">-ResourceGroupName</span></span>
<span data-ttu-id="ea286-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ea286-116">Resource group name.</span></span>

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

### <span data-ttu-id="ea286-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea286-117">CommonParameters</span></span>
<span data-ttu-id="ea286-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea286-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea286-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea286-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea286-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea286-120">INPUTS</span></span>

## <span data-ttu-id="ea286-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea286-121">OUTPUTS</span></span>

### <span data-ttu-id="ea286-122">Microsoft. AzureStack. Management. Storage. admin. modeller. MigrationResult</span><span class="sxs-lookup"><span data-stu-id="ea286-122">Microsoft.AzureStack.Management.Storage.Admin.Models.MigrationResult</span></span>

## <span data-ttu-id="ea286-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea286-123">NOTES</span></span>

## <span data-ttu-id="ea286-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea286-124">RELATED LINKS</span></span>

