---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
ms.openlocfilehash: bcfba4bb002d7982f9a0fb9220fbce24e12e6ffb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594775"
---
# <span data-ttu-id="3dd63-101">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="3dd63-101">Remove-AzureRmDisk</span></span>

## <span data-ttu-id="3dd63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dd63-102">SYNOPSIS</span></span>
<span data-ttu-id="3dd63-103">Diski kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3dd63-103">Removes a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dd63-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3dd63-104">SYNTAX</span></span>

```
Remove-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dd63-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3dd63-105">DESCRIPTION</span></span>
<span data-ttu-id="3dd63-106">**Remove-Azurermdısk** cmdlet 'i diski kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3dd63-106">The **Remove-AzureRmDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="3dd63-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3dd63-107">EXAMPLES</span></span>

### <span data-ttu-id="3dd63-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3dd63-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="3dd63-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Disk01 ' adlı diski kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3dd63-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="3dd63-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3dd63-110">PARAMETERS</span></span>

### <span data-ttu-id="3dd63-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dd63-111">-DefaultProfile</span></span>
<span data-ttu-id="3dd63-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3dd63-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dd63-113">-DiskName</span><span class="sxs-lookup"><span data-stu-id="3dd63-113">-DiskName</span></span>
<span data-ttu-id="3dd63-114">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3dd63-114">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dd63-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3dd63-115">-Force</span></span>
<span data-ttu-id="3dd63-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="3dd63-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3dd63-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dd63-117">-ResourceGroupName</span></span>
<span data-ttu-id="3dd63-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3dd63-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dd63-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="3dd63-119">-Confirm</span></span>
<span data-ttu-id="3dd63-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3dd63-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dd63-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dd63-121">-WhatIf</span></span>
<span data-ttu-id="3dd63-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3dd63-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dd63-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3dd63-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dd63-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dd63-124">CommonParameters</span></span>
<span data-ttu-id="3dd63-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3dd63-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dd63-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dd63-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dd63-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3dd63-127">INPUTS</span></span>

### <span data-ttu-id="3dd63-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3dd63-128">System.String</span></span>

## <span data-ttu-id="3dd63-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3dd63-129">OUTPUTS</span></span>

### <span data-ttu-id="3dd63-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="3dd63-130">System.Object</span></span>

## <span data-ttu-id="3dd63-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3dd63-131">NOTES</span></span>

## <span data-ttu-id="3dd63-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3dd63-132">RELATED LINKS</span></span>

