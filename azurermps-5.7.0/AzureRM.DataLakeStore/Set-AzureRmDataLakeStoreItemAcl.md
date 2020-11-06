---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 313813bec61dac2f5b41f7ad2d36e5ee5ba1b44f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588220"
---
# <span data-ttu-id="c9689-101">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="c9689-101">Set-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="c9689-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9689-102">SYNOPSIS</span></span>
<span data-ttu-id="c9689-103">Data Lake Store 'da bir dosya veya klasörün ACL 'sini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c9689-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9689-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9689-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9689-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9689-105">DESCRIPTION</span></span>
<span data-ttu-id="c9689-106">**Set-AzureRmDataLakeStoreItemAcl** cmdlet 'ı, Data Lake Store 'da bir dosyanın veya klasörün erişim denetim LISTESINI (ACL) değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c9689-106">The **Set-AzureRmDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c9689-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9689-107">EXAMPLES</span></span>

### <span data-ttu-id="c9689-108">Örnek 1: dosya ve klasör için ACL ayarlama</span><span class="sxs-lookup"><span data-stu-id="c9689-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path /
PS C:\> Set-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="c9689-109">İlk komut, ContosoADL hesabının kök dizininin ACL 'sini alır ve $ACL değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c9689-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>

<span data-ttu-id="c9689-110">İkinci komut Test.txt dosya ACL 'sini $ACL olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c9689-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

## <span data-ttu-id="c9689-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9689-111">PARAMETERS</span></span>

### <span data-ttu-id="c9689-112">-Hesap</span><span class="sxs-lookup"><span data-stu-id="c9689-112">-Account</span></span>
<span data-ttu-id="c9689-113">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9689-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="c9689-114">-ACL</span><span class="sxs-lookup"><span data-stu-id="c9689-114">-Acl</span></span>
<span data-ttu-id="c9689-115">Bir dosya veya klasör için ACL belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9689-115">Specifies an ACL for a file or a folder.</span></span>

```yaml
Type: DataLakeStoreItemAce[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9689-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9689-116">-DefaultProfile</span></span>
<span data-ttu-id="c9689-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c9689-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9689-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c9689-118">-PassThru</span></span>
<span data-ttu-id="c9689-119">Sonuç ACL 'sinin döndürülmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9689-119">Indicates the resulting ACL should be returned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9689-120">-Yol</span><span class="sxs-lookup"><span data-stu-id="c9689-120">-Path</span></span>
<span data-ttu-id="c9689-121">Kök dizinden (/) başlayarak dosya veya klasörün veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9689-121">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c9689-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="c9689-122">-Confirm</span></span>
<span data-ttu-id="c9689-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c9689-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9689-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9689-124">-WhatIf</span></span>
<span data-ttu-id="c9689-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9689-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9689-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c9689-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9689-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9689-127">CommonParameters</span></span>
<span data-ttu-id="c9689-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9689-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9689-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9689-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9689-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9689-130">INPUTS</span></span>

### <span data-ttu-id="c9689-131">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="c9689-131">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="c9689-132">' ACL ' parametresi ardışık düzen için ' DataLakeStoreItemAce [] ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c9689-132">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="c9689-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9689-133">OUTPUTS</span></span>

### <span data-ttu-id="c9689-134">'A<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="c9689-134">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="c9689-135">Geçiş belirtildiyse, sonuç olarak ACL girişlerinin sonuç listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="c9689-135">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="c9689-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9689-136">NOTES</span></span>

## <span data-ttu-id="c9689-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9689-137">RELATED LINKS</span></span>

