---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 9339857a125ca0646869a81749f9cf55ff2531ee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752299"
---
# <span data-ttu-id="6f433-101">Remove-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="6f433-101">Remove-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="6f433-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f433-102">SYNOPSIS</span></span>
<span data-ttu-id="6f433-103">Data Lake Store 'da bir dosya veya klasörün ACL 'sini temizler.</span><span class="sxs-lookup"><span data-stu-id="6f433-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="6f433-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f433-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f433-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f433-105">DESCRIPTION</span></span>
<span data-ttu-id="6f433-106">**Remove-AzDataLakeStoreItemAcl** cmdlet 'ı, Data Lake Store 'daki bir dosyanın veya klasörün erişim denetim LISTESINI (ACL) temizler.</span><span class="sxs-lookup"><span data-stu-id="6f433-106">The **Remove-AzDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="6f433-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f433-107">EXAMPLES</span></span>

### <span data-ttu-id="6f433-108">Örnek 1: ACL 'yi klasörden kaldırma</span><span class="sxs-lookup"><span data-stu-id="6f433-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="6f433-109">Bu komut, ContosoADL hesabına ait kök dizinin ACL 'sini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6f433-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="6f433-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f433-110">PARAMETERS</span></span>

### <span data-ttu-id="6f433-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="6f433-111">-Account</span></span>
<span data-ttu-id="6f433-112">Data Lake Store hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f433-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="6f433-113">-Varsayılan</span><span class="sxs-lookup"><span data-stu-id="6f433-113">-Default</span></span>
<span data-ttu-id="6f433-114">Cmdlet 'in bir dosya veya klasör için varsayılan ACL 'yi kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6f433-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f433-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f433-115">-DefaultProfile</span></span>
<span data-ttu-id="6f433-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6f433-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f433-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6f433-117">-Force</span></span>
<span data-ttu-id="6f433-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="6f433-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f433-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6f433-119">-PassThru</span></span>
<span data-ttu-id="6f433-120">Silme işleminin sonucunu belirten bir Boole yanıtının döndürülmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f433-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="6f433-121">-Yol</span><span class="sxs-lookup"><span data-stu-id="6f433-121">-Path</span></span>
<span data-ttu-id="6f433-122">Kök dizinle (/) başlayarak öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f433-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="6f433-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="6f433-123">-Confirm</span></span>
<span data-ttu-id="6f433-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6f433-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f433-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f433-125">-WhatIf</span></span>
<span data-ttu-id="6f433-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6f433-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f433-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6f433-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f433-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f433-128">CommonParameters</span></span>
<span data-ttu-id="6f433-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f433-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f433-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f433-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f433-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f433-131">INPUTS</span></span>

### <span data-ttu-id="6f433-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6f433-132">System.String</span></span>

### <span data-ttu-id="6f433-133">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="6f433-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="6f433-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6f433-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6f433-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f433-135">OUTPUTS</span></span>

### <span data-ttu-id="6f433-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f433-136">System.Boolean</span></span>

## <span data-ttu-id="6f433-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f433-137">NOTES</span></span>
* <span data-ttu-id="6f433-138">Diğer ad: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="6f433-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="6f433-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f433-139">RELATED LINKS</span></span>

[<span data-ttu-id="6f433-140">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6f433-140">Get-AzDataLakeStoreItemAclEntry</span></span>](./Get-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="6f433-141">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="6f433-141">Set-AzDataLakeStoreItemAcl</span></span>](./Set-AzDataLakeStoreItemAcl.md)

[<span data-ttu-id="6f433-142">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6f433-142">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


