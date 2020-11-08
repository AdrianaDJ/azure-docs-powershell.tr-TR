---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 02ff6856cf61664c1bd00e7d88fc7f8de999f2a2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095977"
---
# <span data-ttu-id="5a0cb-101">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5a0cb-101">Get-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="5a0cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a0cb-102">SYNOPSIS</span></span>
<span data-ttu-id="5a0cb-103">Data Lake Store 'da bir dosya veya klasörün ACL 'SI içindeki girdiyi alır.</span><span class="sxs-lookup"><span data-stu-id="5a0cb-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="5a0cb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a0cb-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a0cb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a0cb-105">DESCRIPTION</span></span>
<span data-ttu-id="5a0cb-106">**Get-AzDataLakeStoreItemAclEntry** cmdlet 'ı, Data Lake Store 'daki bir dosyanın veya klasörün erişim denetim LISTESINDE (ACL) bir GIRDI (ACE) alır.</span><span class="sxs-lookup"><span data-stu-id="5a0cb-106">The **Get-AzDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="5a0cb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a0cb-107">EXAMPLES</span></span>

### <span data-ttu-id="5a0cb-108">Örnek 1: klasörün ACL 'sini alma</span><span class="sxs-lookup"><span data-stu-id="5a0cb-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="5a0cb-109">Bu komut belirtilen Data Lake Store hesabının kök dizininin ACL 'sini alır</span><span class="sxs-lookup"><span data-stu-id="5a0cb-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="5a0cb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a0cb-110">PARAMETERS</span></span>

### <span data-ttu-id="5a0cb-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="5a0cb-111">-Account</span></span>
<span data-ttu-id="5a0cb-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a0cb-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="5a0cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a0cb-113">-DefaultProfile</span></span>
<span data-ttu-id="5a0cb-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5a0cb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a0cb-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="5a0cb-115">-Path</span></span>
<span data-ttu-id="5a0cb-116">Kök dizinden (/) başlayarak bu cmdlet 'in ACE aldığı öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a0cb-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="5a0cb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a0cb-117">CommonParameters</span></span>
<span data-ttu-id="5a0cb-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a0cb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a0cb-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a0cb-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a0cb-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a0cb-120">INPUTS</span></span>

### <span data-ttu-id="5a0cb-121">System. String</span><span class="sxs-lookup"><span data-stu-id="5a0cb-121">System.String</span></span>

### <span data-ttu-id="5a0cb-122">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="5a0cb-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="5a0cb-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a0cb-123">OUTPUTS</span></span>

### <span data-ttu-id="5a0cb-124">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="5a0cb-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="5a0cb-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a0cb-125">NOTES</span></span>

## <span data-ttu-id="5a0cb-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a0cb-126">RELATED LINKS</span></span>

[<span data-ttu-id="5a0cb-127">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5a0cb-127">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="5a0cb-128">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5a0cb-128">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


