---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
ms.openlocfilehash: a1b06a870822f2fef0bf2f9a39321c13642f8cad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595019"
---
# <span data-ttu-id="15d01-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="15d01-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="15d01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15d01-102">SYNOPSIS</span></span>
<span data-ttu-id="15d01-103">Diske erişim verir.</span><span class="sxs-lookup"><span data-stu-id="15d01-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15d01-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15d01-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15d01-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="15d01-105">DESCRIPTION</span></span>
<span data-ttu-id="15d01-106">**Grant-AzureRmDiskAccess** cmdlet 'ine bir diske erişim veriyor.</span><span class="sxs-lookup"><span data-stu-id="15d01-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="15d01-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15d01-107">EXAMPLES</span></span>

### <span data-ttu-id="15d01-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="15d01-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="15d01-109">60 saniye için ' ResourceGroup01 ' adındaki kaynak grubundaki ' Disk01 ' adındaki diske ' Read ' erişimi verin.</span><span class="sxs-lookup"><span data-stu-id="15d01-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="15d01-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15d01-110">PARAMETERS</span></span>

### <span data-ttu-id="15d01-111">-Access</span><span class="sxs-lookup"><span data-stu-id="15d01-111">-Access</span></span>
<span data-ttu-id="15d01-112">Erişim düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="15d01-112">Specifies Access level.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15d01-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15d01-113">-DefaultProfile</span></span>
<span data-ttu-id="15d01-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15d01-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15d01-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="15d01-115">-DiskName</span></span>
<span data-ttu-id="15d01-116">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15d01-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="15d01-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="15d01-117">-DurationInSecond</span></span>
<span data-ttu-id="15d01-118">Erişim süresini saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="15d01-118">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15d01-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15d01-119">-ResourceGroupName</span></span>
<span data-ttu-id="15d01-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15d01-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="15d01-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="15d01-121">-Confirm</span></span>
<span data-ttu-id="15d01-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="15d01-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15d01-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15d01-123">-WhatIf</span></span>
<span data-ttu-id="15d01-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="15d01-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15d01-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="15d01-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15d01-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15d01-126">CommonParameters</span></span>
<span data-ttu-id="15d01-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15d01-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15d01-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15d01-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15d01-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15d01-129">INPUTS</span></span>

### <span data-ttu-id="15d01-130">System. String</span><span class="sxs-lookup"><span data-stu-id="15d01-130">System.String</span></span>

## <span data-ttu-id="15d01-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15d01-131">OUTPUTS</span></span>

### <span data-ttu-id="15d01-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="15d01-132">System.Object</span></span>

## <span data-ttu-id="15d01-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15d01-133">NOTES</span></span>

## <span data-ttu-id="15d01-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15d01-134">RELATED LINKS</span></span>

