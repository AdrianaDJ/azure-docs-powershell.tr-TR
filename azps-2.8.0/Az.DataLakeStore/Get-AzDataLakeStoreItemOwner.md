---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: 64af120d793719d4bcd6a24cc3d480cc8f6c104f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752322"
---
# <span data-ttu-id="c743b-101">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="c743b-101">Get-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="c743b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c743b-102">SYNOPSIS</span></span>
<span data-ttu-id="c743b-103">Veri Lake Store 'da bir dosyanın veya klasörün sahibini alır.</span><span class="sxs-lookup"><span data-stu-id="c743b-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c743b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c743b-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c743b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c743b-105">DESCRIPTION</span></span>
<span data-ttu-id="c743b-106">**Get-AzDataLakeStoreItemOwner** cmdlet 'ı Data Lake Store 'da bir dosyanın veya klasörün sahibini alır.</span><span class="sxs-lookup"><span data-stu-id="c743b-106">The **Get-AzDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c743b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c743b-107">EXAMPLES</span></span>

### <span data-ttu-id="c743b-108">Örnek 1: dizinin sahibini alma</span><span class="sxs-lookup"><span data-stu-id="c743b-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="c743b-109">Bu komut, ContosoADL hesabının kök dizininin Kullanıcı sahibini alır.</span><span class="sxs-lookup"><span data-stu-id="c743b-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="c743b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c743b-110">PARAMETERS</span></span>

### <span data-ttu-id="c743b-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="c743b-111">-Account</span></span>
<span data-ttu-id="c743b-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c743b-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="c743b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c743b-113">-DefaultProfile</span></span>
<span data-ttu-id="c743b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c743b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c743b-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="c743b-115">-Path</span></span>
<span data-ttu-id="c743b-116">Kök dizinden (/) başlayarak bir öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c743b-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c743b-117">-Tür</span><span class="sxs-lookup"><span data-stu-id="c743b-117">-Type</span></span>
<span data-ttu-id="c743b-118">Alınacak sahibin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c743b-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="c743b-119">Bu parametre için kabul edilebilir değerler: Kullanıcı ve grup.</span><span class="sxs-lookup"><span data-stu-id="c743b-119">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="c743b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c743b-120">CommonParameters</span></span>
<span data-ttu-id="c743b-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c743b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c743b-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c743b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c743b-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c743b-123">INPUTS</span></span>

### <span data-ttu-id="c743b-124">System. String</span><span class="sxs-lookup"><span data-stu-id="c743b-124">System.String</span></span>

### <span data-ttu-id="c743b-125">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="c743b-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="c743b-126">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="c743b-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="c743b-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c743b-127">OUTPUTS</span></span>

### <span data-ttu-id="c743b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c743b-128">System.String</span></span>

## <span data-ttu-id="c743b-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c743b-129">NOTES</span></span>

## <span data-ttu-id="c743b-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c743b-130">RELATED LINKS</span></span>

[<span data-ttu-id="c743b-131">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="c743b-131">Set-AzDataLakeStoreItemOwner</span></span>](./Set-AzDataLakeStoreItemOwner.md)


