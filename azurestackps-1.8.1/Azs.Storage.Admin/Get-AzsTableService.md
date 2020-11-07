---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf6664023fbd43601c9b7c41a4f578809a9717c5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935156"
---
# <span data-ttu-id="a4442-101">Get-AzsTableService</span><span class="sxs-lookup"><span data-stu-id="a4442-101">Get-AzsTableService</span></span>

## <span data-ttu-id="a4442-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4442-102">SYNOPSIS</span></span>
<span data-ttu-id="a4442-103">Tablo hizmetini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a4442-103">Returns the table service.</span></span>

## <span data-ttu-id="a4442-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a4442-104">SYNTAX</span></span>

```
Get-AzsTableService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="a4442-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a4442-105">DESCRIPTION</span></span>
<span data-ttu-id="a4442-106">Tablo hizmetini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a4442-106">Returns the table service.</span></span>

## <span data-ttu-id="a4442-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a4442-107">EXAMPLES</span></span>

### <span data-ttu-id="a4442-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="a4442-108">EXAMPLE 1</span></span>
```
Get-AzsTableService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="a4442-109">Tablo servıe 'i edinin.</span><span class="sxs-lookup"><span data-stu-id="a4442-109">Get the table servie.</span></span>

## <span data-ttu-id="a4442-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a4442-110">PARAMETERS</span></span>

### <span data-ttu-id="a4442-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="a4442-111">-FarmName</span></span>
<span data-ttu-id="a4442-112">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="a4442-112">Farm Id.</span></span>

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

### <span data-ttu-id="a4442-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4442-113">-ResourceGroupName</span></span>
<span data-ttu-id="a4442-114">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a4442-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4442-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4442-115">CommonParameters</span></span>
<span data-ttu-id="a4442-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a4442-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4442-117">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4442-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4442-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a4442-118">INPUTS</span></span>

## <span data-ttu-id="a4442-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a4442-119">OUTPUTS</span></span>

### <span data-ttu-id="a4442-120">Microsoft. AzureStack. Management. Storage. admin. modeller. TableService</span><span class="sxs-lookup"><span data-stu-id="a4442-120">Microsoft.AzureStack.Management.Storage.Admin.Models.TableService</span></span>

## <span data-ttu-id="a4442-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a4442-121">NOTES</span></span>

## <span data-ttu-id="a4442-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a4442-122">RELATED LINKS</span></span>
