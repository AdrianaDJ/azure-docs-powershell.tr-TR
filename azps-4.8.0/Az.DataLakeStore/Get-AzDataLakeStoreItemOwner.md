---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: ae87c0cc6c9ccea3935e3bd0856d033895070515
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268542"
---
# <span data-ttu-id="14f3c-101">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="14f3c-101">Get-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="14f3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="14f3c-103">Veri Lake Store 'da bir dosyanın veya klasörün sahibini alır.</span><span class="sxs-lookup"><span data-stu-id="14f3c-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="14f3c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="14f3c-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14f3c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="14f3c-105">DESCRIPTION</span></span>
<span data-ttu-id="14f3c-106">**Get-AzDataLakeStoreItemOwner** cmdlet 'ı Data Lake Store 'da bir dosyanın veya klasörün sahibini alır.</span><span class="sxs-lookup"><span data-stu-id="14f3c-106">The **Get-AzDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="14f3c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="14f3c-107">EXAMPLES</span></span>

### <span data-ttu-id="14f3c-108">Örnek 1: dizinin sahibini alma</span><span class="sxs-lookup"><span data-stu-id="14f3c-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="14f3c-109">Bu komut, ContosoADL hesabının kök dizininin Kullanıcı sahibini alır.</span><span class="sxs-lookup"><span data-stu-id="14f3c-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="14f3c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="14f3c-110">PARAMETERS</span></span>

### <span data-ttu-id="14f3c-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="14f3c-111">-Account</span></span>
<span data-ttu-id="14f3c-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="14f3c-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="14f3c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14f3c-113">-DefaultProfile</span></span>
<span data-ttu-id="14f3c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="14f3c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14f3c-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="14f3c-115">-Path</span></span>
<span data-ttu-id="14f3c-116">Kök dizinden (/) başlayarak bir öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="14f3c-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="14f3c-117">-Tür</span><span class="sxs-lookup"><span data-stu-id="14f3c-117">-Type</span></span>
<span data-ttu-id="14f3c-118">Alınacak sahibin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="14f3c-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="14f3c-119">Bu parametre için kabul edilebilir değerler: Kullanıcı ve grup.</span><span class="sxs-lookup"><span data-stu-id="14f3c-119">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="14f3c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14f3c-120">CommonParameters</span></span>
<span data-ttu-id="14f3c-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="14f3c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14f3c-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14f3c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14f3c-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="14f3c-123">INPUTS</span></span>

### <span data-ttu-id="14f3c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="14f3c-124">System.String</span></span>

### <span data-ttu-id="14f3c-125">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="14f3c-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="14f3c-126">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="14f3c-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="14f3c-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="14f3c-127">OUTPUTS</span></span>

### <span data-ttu-id="14f3c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="14f3c-128">System.String</span></span>

## <span data-ttu-id="14f3c-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="14f3c-129">NOTES</span></span>

## <span data-ttu-id="14f3c-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="14f3c-130">RELATED LINKS</span></span>

[<span data-ttu-id="14f3c-131">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="14f3c-131">Set-AzDataLakeStoreItemOwner</span></span>](./Set-AzDataLakeStoreItemOwner.md)


