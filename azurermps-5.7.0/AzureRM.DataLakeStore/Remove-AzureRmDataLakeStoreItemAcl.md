---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 23eb57a6c12c3ce5ba8334b7309b5c282624620a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586711"
---
# <span data-ttu-id="e1128-101">Remove-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="e1128-101">Remove-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="e1128-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1128-102">SYNOPSIS</span></span>
<span data-ttu-id="e1128-103">Data Lake Store 'da bir dosya veya klasörün ACL 'sini temizler.</span><span class="sxs-lookup"><span data-stu-id="e1128-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1128-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e1128-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1128-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e1128-105">DESCRIPTION</span></span>
<span data-ttu-id="e1128-106">**Remove-AzureRmDataLakeStoreItemAcl** cmdlet 'ı, Data Lake Store 'daki bir dosyanın veya klasörün erişim denetim LISTESINI (ACL) temizler.</span><span class="sxs-lookup"><span data-stu-id="e1128-106">The **Remove-AzureRmDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e1128-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e1128-107">EXAMPLES</span></span>

### <span data-ttu-id="e1128-108">Örnek 1: ACL 'yi klasörden kaldırma</span><span class="sxs-lookup"><span data-stu-id="e1128-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="e1128-109">Bu komut, ContosoADL hesabına ait kök dizinin ACL 'sini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e1128-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="e1128-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e1128-110">PARAMETERS</span></span>

### <span data-ttu-id="e1128-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="e1128-111">-Account</span></span>
<span data-ttu-id="e1128-112">Data Lake Store hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1128-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="e1128-113">-Varsayılan</span><span class="sxs-lookup"><span data-stu-id="e1128-113">-Default</span></span>
<span data-ttu-id="e1128-114">Cmdlet 'in bir dosya veya klasör için varsayılan ACL 'yi kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e1128-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1128-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1128-115">-DefaultProfile</span></span>
<span data-ttu-id="e1128-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e1128-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1128-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e1128-117">-Force</span></span>
<span data-ttu-id="e1128-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e1128-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1128-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e1128-119">-PassThru</span></span>
<span data-ttu-id="e1128-120">Silme işleminin sonucunu belirten bir Boole yanıtının döndürülmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1128-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="e1128-121">-Yol</span><span class="sxs-lookup"><span data-stu-id="e1128-121">-Path</span></span>
<span data-ttu-id="e1128-122">Kök dizinle (/) başlayarak öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1128-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="e1128-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="e1128-123">-Confirm</span></span>
<span data-ttu-id="e1128-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e1128-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1128-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1128-125">-WhatIf</span></span>
<span data-ttu-id="e1128-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e1128-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1128-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e1128-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1128-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1128-128">CommonParameters</span></span>
<span data-ttu-id="e1128-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e1128-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1128-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1128-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1128-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e1128-131">INPUTS</span></span>

### <span data-ttu-id="e1128-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e1128-132">None</span></span>
<span data-ttu-id="e1128-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e1128-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e1128-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e1128-134">OUTPUTS</span></span>

### <span data-ttu-id="e1128-135">bool</span><span class="sxs-lookup"><span data-stu-id="e1128-135">bool</span></span>
<span data-ttu-id="e1128-136">Geçiş belirtildiyse, başarılı bir tamamlandığında doğru sonucunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="e1128-136">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="e1128-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e1128-137">NOTES</span></span>
* <span data-ttu-id="e1128-138">Diğer ad: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="e1128-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="e1128-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e1128-139">RELATED LINKS</span></span>

[<span data-ttu-id="e1128-140">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e1128-140">Get-AzureRmDataLakeStoreItemAclEntry</span></span>](./Get-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="e1128-141">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="e1128-141">Set-AzureRmDataLakeStoreItemAcl</span></span>](./Set-AzureRmDataLakeStoreItemAcl.md)

[<span data-ttu-id="e1128-142">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e1128-142">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


