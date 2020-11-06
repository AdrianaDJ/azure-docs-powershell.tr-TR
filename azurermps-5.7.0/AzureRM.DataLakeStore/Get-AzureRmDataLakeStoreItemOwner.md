---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: 886c8e7227d036e67d3e6f0d2dc04c4e9887e777
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588940"
---
# <span data-ttu-id="2e374-101">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="2e374-101">Get-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="2e374-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e374-102">SYNOPSIS</span></span>
<span data-ttu-id="2e374-103">Veri Lake Store 'da bir dosyanın veya klasörün sahibini alır.</span><span class="sxs-lookup"><span data-stu-id="2e374-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e374-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e374-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e374-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e374-105">DESCRIPTION</span></span>
<span data-ttu-id="2e374-106">**Get-AzureRmDataLakeStoreItemOwner** cmdlet 'ı Data Lake Store 'da bir dosyanın veya klasörün sahibini alır.</span><span class="sxs-lookup"><span data-stu-id="2e374-106">The **Get-AzureRmDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="2e374-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e374-107">EXAMPLES</span></span>

### <span data-ttu-id="2e374-108">Örnek 1: dizinin sahibini alma</span><span class="sxs-lookup"><span data-stu-id="2e374-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="2e374-109">Bu komut, ContosoADL hesabının kök dizininin Kullanıcı sahibini alır.</span><span class="sxs-lookup"><span data-stu-id="2e374-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="2e374-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e374-110">PARAMETERS</span></span>

### <span data-ttu-id="2e374-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="2e374-111">-Account</span></span>
<span data-ttu-id="2e374-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e374-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e374-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e374-113">-DefaultProfile</span></span>
<span data-ttu-id="2e374-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2e374-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e374-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="2e374-115">-Path</span></span>
<span data-ttu-id="2e374-116">Kök dizinden (/) başlayarak bir öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e374-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e374-117">-Tür</span><span class="sxs-lookup"><span data-stu-id="2e374-117">-Type</span></span>
<span data-ttu-id="2e374-118">Alınacak sahibin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e374-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="2e374-119">Bu parametre için kabul edilebilir değerler: Kullanıcı ve grup.</span><span class="sxs-lookup"><span data-stu-id="2e374-119">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Owner
Parameter Sets: (All)
Aliases: 
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e374-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e374-120">CommonParameters</span></span>
<span data-ttu-id="2e374-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e374-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e374-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e374-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e374-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e374-123">INPUTS</span></span>

### <span data-ttu-id="2e374-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2e374-124">None</span></span>
<span data-ttu-id="2e374-125">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="2e374-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2e374-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e374-126">OUTPUTS</span></span>

### <span data-ttu-id="2e374-127">dizisi</span><span class="sxs-lookup"><span data-stu-id="2e374-127">string</span></span>
<span data-ttu-id="2e374-128">Belirtilen öğenin sahibi.</span><span class="sxs-lookup"><span data-stu-id="2e374-128">The owner of the specified item.</span></span>

## <span data-ttu-id="2e374-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e374-129">NOTES</span></span>

## <span data-ttu-id="2e374-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e374-130">RELATED LINKS</span></span>

[<span data-ttu-id="2e374-131">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="2e374-131">Set-AzureRmDataLakeStoreItemOwner</span></span>](./Set-AzureRmDataLakeStoreItemOwner.md)


