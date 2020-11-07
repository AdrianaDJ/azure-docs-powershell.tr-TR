---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 94f81e8256af9282cdd5e09c1ab2822bf99c772f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764563"
---
# <span data-ttu-id="454ea-101">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="454ea-101">Set-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="454ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="454ea-102">SYNOPSIS</span></span>
<span data-ttu-id="454ea-103">Data Lake Store 'da bir dosya veya klasörün ACL 'sini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="454ea-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="454ea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="454ea-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="454ea-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="454ea-105">DESCRIPTION</span></span>
<span data-ttu-id="454ea-106">**Set-AzureRmDataLakeStoreItemAcl** cmdlet 'ı, Data Lake Store 'da bir dosyanın veya klasörün erişim denetim LISTESINI (ACL) değiştirir.</span><span class="sxs-lookup"><span data-stu-id="454ea-106">The **Set-AzureRmDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="454ea-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="454ea-107">EXAMPLES</span></span>

### <span data-ttu-id="454ea-108">Örnek 1: dosya ve klasör için ACL ayarlama</span><span class="sxs-lookup"><span data-stu-id="454ea-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path /
PS C:\> Set-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="454ea-109">İlk komut, ContosoADL hesabının kök dizininin ACL 'sini alır ve $ACL değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="454ea-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>

<span data-ttu-id="454ea-110">İkinci komut Test.txt dosya ACL 'sini $ACL olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="454ea-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

## <span data-ttu-id="454ea-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="454ea-111">PARAMETERS</span></span>

### <span data-ttu-id="454ea-112">-Hesap</span><span class="sxs-lookup"><span data-stu-id="454ea-112">-Account</span></span>
<span data-ttu-id="454ea-113">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="454ea-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="454ea-114">-ACL</span><span class="sxs-lookup"><span data-stu-id="454ea-114">-Acl</span></span>
<span data-ttu-id="454ea-115">Bir dosya veya klasör için ACL belirtir.</span><span class="sxs-lookup"><span data-stu-id="454ea-115">Specifies an ACL for a file or a folder.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="454ea-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="454ea-116">-PassThru</span></span>
<span data-ttu-id="454ea-117">Sonuç ACL 'sinin döndürülmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="454ea-117">Indicates the resulting ACL should be returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="454ea-118">-Yol</span><span class="sxs-lookup"><span data-stu-id="454ea-118">-Path</span></span>
<span data-ttu-id="454ea-119">Kök dizinden (/) başlayarak dosya veya klasörün veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="454ea-119">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="454ea-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="454ea-120">-Confirm</span></span>
<span data-ttu-id="454ea-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="454ea-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="454ea-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="454ea-122">-WhatIf</span></span>
<span data-ttu-id="454ea-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="454ea-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="454ea-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="454ea-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="454ea-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="454ea-125">-DefaultProfile</span></span>
<span data-ttu-id="454ea-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="454ea-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="454ea-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="454ea-127">CommonParameters</span></span>
<span data-ttu-id="454ea-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="454ea-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="454ea-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="454ea-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="454ea-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="454ea-130">INPUTS</span></span>

### <span data-ttu-id="454ea-131">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="454ea-131">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="454ea-132">' ACL ' parametresi ardışık düzen için ' DataLakeStoreItemAce [] ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="454ea-132">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="454ea-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="454ea-133">OUTPUTS</span></span>

### <span data-ttu-id="454ea-134">'A<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="454ea-134">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="454ea-135">Geçiş belirtildiyse, sonuç olarak ACL girişlerinin sonuç listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="454ea-135">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="454ea-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="454ea-136">NOTES</span></span>

## <span data-ttu-id="454ea-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="454ea-137">RELATED LINKS</span></span>

