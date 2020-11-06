---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 8473cc65ec6afffb9433159d848d9e7b8629a351
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591979"
---
# <span data-ttu-id="f1f3c-101">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f1f3c-101">Get-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="f1f3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f3c-103">Data Lake Store 'da bir dosya veya klasörün ACL 'SI içindeki girdiyi alır.</span><span class="sxs-lookup"><span data-stu-id="f1f3c-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1f3c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1f3c-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1f3c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1f3c-105">DESCRIPTION</span></span>
<span data-ttu-id="f1f3c-106">**Get-AzureRmDataLakeStoreItemAclEntry** cmdlet 'ı, Data Lake Store 'daki bir dosyanın veya klasörün erişim denetim LISTESINDE (ACL) bir GIRDI (ACE) alır.</span><span class="sxs-lookup"><span data-stu-id="f1f3c-106">The **Get-AzureRmDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f1f3c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1f3c-107">EXAMPLES</span></span>

### <span data-ttu-id="f1f3c-108">Örnek 1: klasörün ACL 'sini alma</span><span class="sxs-lookup"><span data-stu-id="f1f3c-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="f1f3c-109">Bu komut belirtilen Data Lake Store hesabının kök dizininin ACL 'sini alır</span><span class="sxs-lookup"><span data-stu-id="f1f3c-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="f1f3c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1f3c-110">PARAMETERS</span></span>

### <span data-ttu-id="f1f3c-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="f1f3c-111">-Account</span></span>
<span data-ttu-id="f1f3c-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1f3c-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f1f3c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1f3c-113">-DefaultProfile</span></span>
<span data-ttu-id="f1f3c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1f3c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1f3c-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="f1f3c-115">-Path</span></span>
<span data-ttu-id="f1f3c-116">Kök dizinden (/) başlayarak bu cmdlet 'in ACE aldığı öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1f3c-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="f1f3c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f3c-117">CommonParameters</span></span>
<span data-ttu-id="f1f3c-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1f3c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f3c-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1f3c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f3c-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1f3c-120">INPUTS</span></span>

### <span data-ttu-id="f1f3c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f1f3c-121">System.String</span></span>

### <span data-ttu-id="f1f3c-122">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="f1f3c-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="f1f3c-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1f3c-123">OUTPUTS</span></span>

### <span data-ttu-id="f1f3c-124">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="f1f3c-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="f1f3c-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1f3c-125">NOTES</span></span>

## <span data-ttu-id="f1f3c-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1f3c-126">RELATED LINKS</span></span>

[<span data-ttu-id="f1f3c-127">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f1f3c-127">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="f1f3c-128">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f1f3c-128">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


