---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
ms.openlocfilehash: d969dcc0906def107b68a76980b39482dfe8c4e4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936197"
---
# <span data-ttu-id="259b1-101">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="259b1-101">Remove-AzStorageAccount</span></span>

## <span data-ttu-id="259b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="259b1-102">SYNOPSIS</span></span>
<span data-ttu-id="259b1-103">Azure 'dan depolama hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="259b1-103">Removes a Storage account from Azure.</span></span>

## <span data-ttu-id="259b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="259b1-104">SYNTAX</span></span>

```
Remove-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="259b1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="259b1-105">DESCRIPTION</span></span>
<span data-ttu-id="259b1-106">**Remove-AzStorageAccount** cmdlet 'i Azure 'Dan bir depolama hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="259b1-106">The **Remove-AzStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="259b1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="259b1-107">EXAMPLES</span></span>

### <span data-ttu-id="259b1-108">Örnek 1: depolama hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="259b1-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="259b1-109">Bu komut belirtilen depolama hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="259b1-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="259b1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="259b1-110">PARAMETERS</span></span>

### <span data-ttu-id="259b1-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="259b1-111">-AsJob</span></span>
<span data-ttu-id="259b1-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="259b1-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="259b1-113">-DefaultProfile</span></span>
<span data-ttu-id="259b1-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="259b1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="259b1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="259b1-115">-Force</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259b1-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="259b1-116">-Name</span></span>
<span data-ttu-id="259b1-117">Kaldırılacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="259b1-117">Specifies the name of the Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="259b1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="259b1-118">-ResourceGroupName</span></span>
<span data-ttu-id="259b1-119">Kaldırılacak depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="259b1-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="259b1-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="259b1-120">-Confirm</span></span>
<span data-ttu-id="259b1-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="259b1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="259b1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="259b1-122">-WhatIf</span></span>
<span data-ttu-id="259b1-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="259b1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="259b1-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="259b1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="259b1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="259b1-125">CommonParameters</span></span>
<span data-ttu-id="259b1-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="259b1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="259b1-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="259b1-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="259b1-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="259b1-128">INPUTS</span></span>

### <span data-ttu-id="259b1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="259b1-129">System.String</span></span>

## <span data-ttu-id="259b1-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="259b1-130">OUTPUTS</span></span>

### <span data-ttu-id="259b1-131">System. void</span><span class="sxs-lookup"><span data-stu-id="259b1-131">System.Void</span></span>

## <span data-ttu-id="259b1-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="259b1-132">NOTES</span></span>

## <span data-ttu-id="259b1-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="259b1-133">RELATED LINKS</span></span>

[<span data-ttu-id="259b1-134">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="259b1-134">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="259b1-135">Yeni-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="259b1-135">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="259b1-136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="259b1-136">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


