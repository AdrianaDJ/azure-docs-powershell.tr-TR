---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 2532b8fb63fb864cf2c70b9e2bfd1d5ef1a5365e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763753"
---
# <span data-ttu-id="037d5-101">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="037d5-101">Get-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="037d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="037d5-102">SYNOPSIS</span></span>
<span data-ttu-id="037d5-103">Data Lake Store 'da bir dosya veya klasörün ACL 'SI içindeki girdiyi alır.</span><span class="sxs-lookup"><span data-stu-id="037d5-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="037d5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="037d5-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="037d5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="037d5-105">DESCRIPTION</span></span>
<span data-ttu-id="037d5-106">**Get-AzureRmDataLakeStoreItemAclEntry** cmdlet 'ı, Data Lake Store 'daki bir dosyanın veya klasörün erişim denetim LISTESINDE (ACL) bir GIRDI (ACE) alır.</span><span class="sxs-lookup"><span data-stu-id="037d5-106">The **Get-AzureRmDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="037d5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="037d5-107">EXAMPLES</span></span>

### <span data-ttu-id="037d5-108">Örnek 1: klasörün ACL 'sini alma</span><span class="sxs-lookup"><span data-stu-id="037d5-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="037d5-109">Bu komut belirtilen Data Lake Store hesabının kök dizininin ACL 'sini alır</span><span class="sxs-lookup"><span data-stu-id="037d5-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="037d5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="037d5-110">PARAMETERS</span></span>

### <span data-ttu-id="037d5-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="037d5-111">-Account</span></span>
<span data-ttu-id="037d5-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="037d5-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="037d5-113">-Yol</span><span class="sxs-lookup"><span data-stu-id="037d5-113">-Path</span></span>
<span data-ttu-id="037d5-114">Kök dizinden (/) başlayarak bu cmdlet 'in ACE aldığı öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="037d5-114">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="037d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="037d5-115">-DefaultProfile</span></span>
<span data-ttu-id="037d5-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="037d5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="037d5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="037d5-117">CommonParameters</span></span>
<span data-ttu-id="037d5-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="037d5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="037d5-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="037d5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="037d5-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="037d5-120">INPUTS</span></span>

## <span data-ttu-id="037d5-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="037d5-121">OUTPUTS</span></span>

### <span data-ttu-id="037d5-122">'A<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="037d5-122">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="037d5-123">Belirtilen klasör veya dosya için ACL girişlerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="037d5-123">The list of ACL entries for the specified folder or file.</span></span>

## <span data-ttu-id="037d5-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="037d5-124">NOTES</span></span>

## <span data-ttu-id="037d5-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="037d5-125">RELATED LINKS</span></span>

[<span data-ttu-id="037d5-126">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="037d5-126">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="037d5-127">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="037d5-127">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


