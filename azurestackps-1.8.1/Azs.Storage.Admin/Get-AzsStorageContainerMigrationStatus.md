---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 96220d7bac0a71f579f81a4d01f4f1dc3cba9dd1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935053"
---
# <span data-ttu-id="75aca-101">Get-AzsStorageContainerMigrationStatus</span><span class="sxs-lookup"><span data-stu-id="75aca-101">Get-AzsStorageContainerMigrationStatus</span></span>

## <span data-ttu-id="75aca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75aca-102">SYNOPSIS</span></span>
<span data-ttu-id="75aca-103">Kapsayıcı geçiş işinin durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="75aca-103">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="75aca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75aca-104">SYNTAX</span></span>

```
Get-AzsStorageContainerMigrationStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="75aca-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="75aca-105">DESCRIPTION</span></span>
<span data-ttu-id="75aca-106">Kapsayıcı geçiş işinin durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="75aca-106">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="75aca-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75aca-107">EXAMPLES</span></span>

### <span data-ttu-id="75aca-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="75aca-108">EXAMPLE 1</span></span>
```
Get-AzsStorageContainerMigrationStatus -FarmName "6ed442a3-ec47-4145-b2f0-9b90377b01d0" -JobId "6478ef3b-b7d5-4827-8d47-551c6afb9dd4"
```

<span data-ttu-id="75aca-109">Kapsayıcı geçiş işinin durumunu edinin.</span><span class="sxs-lookup"><span data-stu-id="75aca-109">Get the status of a container migration job.</span></span>

## <span data-ttu-id="75aca-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75aca-110">PARAMETERS</span></span>

### <span data-ttu-id="75aca-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="75aca-111">-FarmName</span></span>
<span data-ttu-id="75aca-112">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="75aca-112">Farm Id.</span></span>

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

### <span data-ttu-id="75aca-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="75aca-113">-JobId</span></span>
<span data-ttu-id="75aca-114">İşlem kimliği.</span><span class="sxs-lookup"><span data-stu-id="75aca-114">Operation Id.</span></span>

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

### <span data-ttu-id="75aca-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75aca-115">-ResourceGroupName</span></span>
<span data-ttu-id="75aca-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="75aca-116">Resource group name.</span></span>

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

### <span data-ttu-id="75aca-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75aca-117">CommonParameters</span></span>
<span data-ttu-id="75aca-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75aca-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75aca-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75aca-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75aca-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75aca-120">INPUTS</span></span>

## <span data-ttu-id="75aca-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75aca-121">OUTPUTS</span></span>

### <span data-ttu-id="75aca-122">Microsoft. AzureStack. Management. Storage. admin. modeller. MigrationResult</span><span class="sxs-lookup"><span data-stu-id="75aca-122">Microsoft.AzureStack.Management.Storage.Admin.Models.MigrationResult</span></span>

## <span data-ttu-id="75aca-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75aca-123">NOTES</span></span>

## <span data-ttu-id="75aca-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75aca-124">RELATED LINKS</span></span>
