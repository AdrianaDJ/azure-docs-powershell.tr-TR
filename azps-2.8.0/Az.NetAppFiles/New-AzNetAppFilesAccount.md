---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 7d45b80efd0996050b2814b2d1d28af1d9c6a43f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931858"
---
# <span data-ttu-id="745b9-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="745b9-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="745b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="745b9-102">SYNOPSIS</span></span>
<span data-ttu-id="745b9-103">Yeni bir Azure NetApp dosyaları (ANF) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="745b9-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="745b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="745b9-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="745b9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="745b9-105">DESCRIPTION</span></span>
<span data-ttu-id="745b9-106">**New-AzNetAppFilesAccount** cmdlet 'ı BIR ANF hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="745b9-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="745b9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="745b9-107">EXAMPLES</span></span>

### <span data-ttu-id="745b9-108">Örnek 1: ANF hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="745b9-108">Example 1: Create an ANF account</span></span>
```
PS C:\>New-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount" -l "westus2"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="745b9-109">Bu komut, "MyAnfAccount" yeni ANF hesabını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="745b9-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="745b9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="745b9-110">PARAMETERS</span></span>

### <span data-ttu-id="745b9-111">-Activedizinler</span><span class="sxs-lookup"><span data-stu-id="745b9-111">-ActiveDirectories</span></span>
<span data-ttu-id="745b9-112">Active Directory 'yi temsil eden bir Hashtable dizisi</span><span class="sxs-lookup"><span data-stu-id="745b9-112">A hashtable array which represents the active directories</span></span>

```yaml
Type: PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="745b9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="745b9-113">-DefaultProfile</span></span>
<span data-ttu-id="745b9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="745b9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="745b9-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="745b9-115">-Location</span></span>
<span data-ttu-id="745b9-116">Kaynağın konumu</span><span class="sxs-lookup"><span data-stu-id="745b9-116">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="745b9-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="745b9-117">-Name</span></span>
<span data-ttu-id="745b9-118">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="745b9-118">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="745b9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="745b9-119">-ResourceGroupName</span></span>
<span data-ttu-id="745b9-120">ANF hesabının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="745b9-120">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="745b9-121">Etiketli</span><span class="sxs-lookup"><span data-stu-id="745b9-121">-Tag</span></span>
<span data-ttu-id="745b9-122">Kaynak etiketlerini temsil eden bir Hashtable</span><span class="sxs-lookup"><span data-stu-id="745b9-122">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="745b9-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="745b9-123">-Confirm</span></span>
<span data-ttu-id="745b9-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="745b9-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="745b9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="745b9-125">-WhatIf</span></span>
<span data-ttu-id="745b9-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="745b9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="745b9-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="745b9-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="745b9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="745b9-128">CommonParameters</span></span>
<span data-ttu-id="745b9-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="745b9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="745b9-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="745b9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="745b9-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="745b9-131">INPUTS</span></span>

### <span data-ttu-id="745b9-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="745b9-132">None</span></span>

## <span data-ttu-id="745b9-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="745b9-133">OUTPUTS</span></span>

### <span data-ttu-id="745b9-134">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="745b9-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="745b9-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="745b9-135">NOTES</span></span>

## <span data-ttu-id="745b9-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="745b9-136">RELATED LINKS</span></span>
