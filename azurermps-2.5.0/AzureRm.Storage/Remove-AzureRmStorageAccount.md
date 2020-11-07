---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstorageaccount
schema: 2.0.0
ms.openlocfilehash: d3e7a04f292be8e83bc28456c0510450c078a777
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939986"
---
# <span data-ttu-id="1ad6b-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ad6b-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="1ad6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ad6b-102">SYNOPSIS</span></span>
<span data-ttu-id="1ad6b-103">Azure 'dan depolama hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ad6b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ad6b-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ad6b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ad6b-105">DESCRIPTION</span></span>
<span data-ttu-id="1ad6b-106">**Remove-AzureRmStorageAccount** cmdlet 'i Azure 'Dan bir depolama hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="1ad6b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ad6b-107">EXAMPLES</span></span>

### <span data-ttu-id="1ad6b-108">Örnek 1: depolama hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="1ad6b-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="1ad6b-109">Bu komut belirtilen depolama hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="1ad6b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ad6b-110">PARAMETERS</span></span>

### <span data-ttu-id="1ad6b-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="1ad6b-111">-AsJob</span></span>
<span data-ttu-id="1ad6b-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1ad6b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ad6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ad6b-113">-DefaultProfile</span></span>
<span data-ttu-id="1ad6b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ad6b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1ad6b-115">-Force</span></span>
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

### <span data-ttu-id="1ad6b-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="1ad6b-116">-Name</span></span>
<span data-ttu-id="1ad6b-117">Kaldırılacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-117">Specifies the name of the Storage account to remove.</span></span>

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

### <span data-ttu-id="1ad6b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ad6b-118">-ResourceGroupName</span></span>
<span data-ttu-id="1ad6b-119">Kaldırılacak depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="1ad6b-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="1ad6b-120">-Confirm</span></span>
<span data-ttu-id="1ad6b-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ad6b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ad6b-122">-WhatIf</span></span>
<span data-ttu-id="1ad6b-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ad6b-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ad6b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ad6b-125">CommonParameters</span></span>
<span data-ttu-id="1ad6b-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ad6b-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ad6b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ad6b-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ad6b-128">INPUTS</span></span>

### <span data-ttu-id="1ad6b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1ad6b-129">System.String</span></span>

## <span data-ttu-id="1ad6b-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ad6b-130">OUTPUTS</span></span>

### <span data-ttu-id="1ad6b-131">System. void</span><span class="sxs-lookup"><span data-stu-id="1ad6b-131">System.Void</span></span>

## <span data-ttu-id="1ad6b-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ad6b-132">NOTES</span></span>

## <span data-ttu-id="1ad6b-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ad6b-133">RELATED LINKS</span></span>

[<span data-ttu-id="1ad6b-134">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ad6b-134">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="1ad6b-135">Yeni-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ad6b-135">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="1ad6b-136">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ad6b-136">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


