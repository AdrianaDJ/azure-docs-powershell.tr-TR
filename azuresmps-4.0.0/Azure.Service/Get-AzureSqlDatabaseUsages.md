---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 9953AF91-2424-4BD1-9133-E0E07AC1087E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a17ff5e4ec976fcf0c6be02e3fbc373d7ffd2f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106563"
---
# <span data-ttu-id="bfe6f-101">Get-AzureSqlDatabaseUsages</span><span class="sxs-lookup"><span data-stu-id="bfe6f-101">Get-AzureSqlDatabaseUsages</span></span>

## <span data-ttu-id="bfe6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfe6f-102">SYNOPSIS</span></span>
<span data-ttu-id="bfe6f-103">SQL veritabanının boyut ve boyut sınırını alır.</span><span class="sxs-lookup"><span data-stu-id="bfe6f-103">Gets the size and size limit of a SQL Database.</span></span>

## <span data-ttu-id="bfe6f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bfe6f-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseUsages -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="bfe6f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bfe6f-105">DESCRIPTION</span></span>
<span data-ttu-id="bfe6f-106">**Get-Azuressqldatabasekullanımlarının** cmdlet 'i, BIR Azure SQL veritabanının geçerli boyut ve boyut sınırını alır.</span><span class="sxs-lookup"><span data-stu-id="bfe6f-106">The **Get-AzureSqlDatabaseUsages** cmdlet gets the current size and size limit of an Azure SQL Database.</span></span>

## <span data-ttu-id="bfe6f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bfe6f-107">EXAMPLES</span></span>

### <span data-ttu-id="bfe6f-108">Örnek 1: SQL veritabanı için kullanım bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="bfe6f-108">Example 1: Get usage information for a SQL Database</span></span>
```
PS C:\> Get-AzureSqlDatabaseUsages -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="bfe6f-109">Bu komut, Server01 üzerinde Database01 adındaki SQL veritabanı için boyut ve boyut sınırı bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="bfe6f-109">This command gets the size and size limit information for the SQL Database named Database01 on Server01.</span></span>

## <span data-ttu-id="bfe6f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bfe6f-110">PARAMETERS</span></span>

### <span data-ttu-id="bfe6f-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bfe6f-111">-DatabaseName</span></span>
<span data-ttu-id="bfe6f-112">Azure SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfe6f-112">Specifies the name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfe6f-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="bfe6f-113">-Profile</span></span>
<span data-ttu-id="bfe6f-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfe6f-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bfe6f-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="bfe6f-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfe6f-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bfe6f-116">-ServerName</span></span>
<span data-ttu-id="bfe6f-117">Azure SQL veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfe6f-117">Specifies the name of the server that hosts the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe6f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfe6f-118">CommonParameters</span></span>
<span data-ttu-id="bfe6f-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bfe6f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfe6f-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfe6f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfe6f-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bfe6f-121">INPUTS</span></span>

## <span data-ttu-id="bfe6f-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bfe6f-122">OUTPUTS</span></span>

## <span data-ttu-id="bfe6f-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bfe6f-123">NOTES</span></span>

## <span data-ttu-id="bfe6f-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bfe6f-124">RELATED LINKS</span></span>

