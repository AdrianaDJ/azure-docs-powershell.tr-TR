---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 3b433860cda56f827bb58bc135240da41b89ef93
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266348"
---
# <span data-ttu-id="3a9f7-101">Set-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a9f7-101">Set-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="3a9f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a9f7-102">SYNOPSIS</span></span>
<span data-ttu-id="3a9f7-103">Etkin kiracı SQL bilgileri koruma ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3a9f7-103">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="3a9f7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a9f7-104">SYNTAX</span></span>

### <span data-ttu-id="3a9f7-105">SQL Information Protection Ilkesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3a9f7-105">SQL Information Protection Policy (Default)</span></span>
```
Set-AzSqlInformationProtectionPolicy -Policy <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a9f7-106">SQL Information Protection Ilke dosyası yolu</span><span class="sxs-lookup"><span data-stu-id="3a9f7-106">SQL Information Protection Policy File Path</span></span>
```
Set-AzSqlInformationProtectionPolicy -FilePath <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a9f7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a9f7-107">DESCRIPTION</span></span>
<span data-ttu-id="3a9f7-108">Etkin kiracı SQL bilgileri koruma ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3a9f7-108">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="3a9f7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a9f7-109">EXAMPLES</span></span>

### <span data-ttu-id="3a9f7-110">Örnekteki</span><span class="sxs-lookup"><span data-stu-id="3a9f7-110">Example</span></span>
```powershell
PS C:\> Set-AzSqlInformationProtectionPolicy -FilePath "C:\Users\myUser\Desktop\policy.json"
```

## <span data-ttu-id="3a9f7-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a9f7-111">PARAMETERS</span></span>

### <span data-ttu-id="3a9f7-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="3a9f7-112">-AsJob</span></span>
<span data-ttu-id="3a9f7-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3a9f7-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a9f7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a9f7-114">-DefaultProfile</span></span>
<span data-ttu-id="3a9f7-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3a9f7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a9f7-116">-DosyaYolu</span><span class="sxs-lookup"><span data-stu-id="3a9f7-116">-FilePath</span></span>
<span data-ttu-id="3a9f7-117">SQL Information Protection Ilke tanımını içeren bir. json dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a9f7-117">Specifies a path of a .json file containing SQL Information Protection Policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: SQL Information Protection Policy File Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a9f7-118">-İlke</span><span class="sxs-lookup"><span data-stu-id="3a9f7-118">-Policy</span></span>
<span data-ttu-id="3a9f7-119">SQL Information Protection ilke tanımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a9f7-119">Specifies a SQL information protection policy definition.</span></span> <span data-ttu-id="3a9f7-120">Bir. json dosyasının veya ilkeyi tanımlayan JSON biçim dizesinin yolunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3a9f7-120">You can specify a path of a .json file or a JSON format string that defines the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SQL Information Protection Policy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a9f7-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="3a9f7-121">-Confirm</span></span>
<span data-ttu-id="3a9f7-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3a9f7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a9f7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a9f7-123">-WhatIf</span></span>
<span data-ttu-id="3a9f7-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3a9f7-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a9f7-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3a9f7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a9f7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a9f7-126">CommonParameters</span></span>
<span data-ttu-id="3a9f7-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a9f7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a9f7-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3a9f7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a9f7-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a9f7-129">INPUTS</span></span>

### <span data-ttu-id="3a9f7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3a9f7-130">System.String</span></span>

## <span data-ttu-id="3a9f7-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a9f7-131">OUTPUTS</span></span>

### <span data-ttu-id="3a9f7-132">Microsoft. Azure. Commands. Securitcenter. model. SqlInformationProtectionPolicy. PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a9f7-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="3a9f7-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a9f7-133">NOTES</span></span>

## <span data-ttu-id="3a9f7-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a9f7-134">RELATED LINKS</span></span>
