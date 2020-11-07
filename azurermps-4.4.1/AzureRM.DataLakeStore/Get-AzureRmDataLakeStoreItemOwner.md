---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: 5c36257050cccf217234a3b1ef6b89120e36b3c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763752"
---
# <span data-ttu-id="31444-101">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="31444-101">Get-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="31444-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31444-102">SYNOPSIS</span></span>
<span data-ttu-id="31444-103">Veri Lake Store 'da bir dosyanın veya klasörün sahibini alır.</span><span class="sxs-lookup"><span data-stu-id="31444-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31444-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31444-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31444-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="31444-105">DESCRIPTION</span></span>
<span data-ttu-id="31444-106">**Get-AzureRmDataLakeStoreItemOwner** cmdlet 'ı Data Lake Store 'da bir dosyanın veya klasörün sahibini alır.</span><span class="sxs-lookup"><span data-stu-id="31444-106">The **Get-AzureRmDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="31444-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31444-107">EXAMPLES</span></span>

### <span data-ttu-id="31444-108">Örnek 1: dizinin sahibini alma</span><span class="sxs-lookup"><span data-stu-id="31444-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="31444-109">Bu komut, ContosoADL hesabının kök dizininin Kullanıcı sahibini alır.</span><span class="sxs-lookup"><span data-stu-id="31444-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="31444-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31444-110">PARAMETERS</span></span>

### <span data-ttu-id="31444-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="31444-111">-Account</span></span>
<span data-ttu-id="31444-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="31444-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31444-113">-Yol</span><span class="sxs-lookup"><span data-stu-id="31444-113">-Path</span></span>
<span data-ttu-id="31444-114">Kök dizinden (/) başlayarak bir öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="31444-114">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31444-115">-Tür</span><span class="sxs-lookup"><span data-stu-id="31444-115">-Type</span></span>
<span data-ttu-id="31444-116">Alınacak sahibin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="31444-116">Specifies the type of owner to get.</span></span>
<span data-ttu-id="31444-117">Bu parametre için kabul edilebilir değerler: Kullanıcı ve grup.</span><span class="sxs-lookup"><span data-stu-id="31444-117">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases: 
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31444-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31444-118">-DefaultProfile</span></span>
<span data-ttu-id="31444-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="31444-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31444-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31444-120">CommonParameters</span></span>
<span data-ttu-id="31444-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31444-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31444-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31444-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31444-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31444-123">INPUTS</span></span>

## <span data-ttu-id="31444-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31444-124">OUTPUTS</span></span>

### <span data-ttu-id="31444-125">dizisi</span><span class="sxs-lookup"><span data-stu-id="31444-125">string</span></span>
<span data-ttu-id="31444-126">Belirtilen öğenin sahibi.</span><span class="sxs-lookup"><span data-stu-id="31444-126">The owner of the specified item.</span></span>

## <span data-ttu-id="31444-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31444-127">NOTES</span></span>

## <span data-ttu-id="31444-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31444-128">RELATED LINKS</span></span>

[<span data-ttu-id="31444-129">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="31444-129">Set-AzureRmDataLakeStoreItemOwner</span></span>](./Set-AzureRmDataLakeStoreItemOwner.md)


